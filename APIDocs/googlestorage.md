package googlestorage
    import "github.com/scorelab/gocloud-v2/storage/googlestorage"


FUNCTIONS

func Attachdiskdictnoaryconvert(option Attachdisk, Attachdiskjsonmap map[string]interface{})

func Creatediskdictnoaryconvert(option Creatdisk, Creatdiskjsonmap map[string]interface{})

func Createsnapshotdictnoaryconvert(option Snapshot, Createsnapshotjsonmap map[string]interface{})

TYPES

type Attachdisk struct {
    Source             string            `json:"source"`
    DeviceName         string            `json:"deviceName"`
    AutoDelete         bool              `json:"autoDelete"`
    Boot               bool              `json:"boot"`
    DiskEncryptionKeys DiskEncryptionKey `json:"diskEncryptionKey"`
    Index              int               `json:"index"`
    Interface          string            `json:"interface"`
    Kind               string            `json:"kind"`
    Licenses           []string          `json:"licenses"`
    Mode               string            `json:"mode"`
    Type               string            `json:"type"`
    InitializeParam    InitializeParams  `json:"initializeParams"`
}

type Creatdisk struct {
    Name                         string                      `json:"name"`
    Type                         string                      `json:"type"`
    Zone                         string                      `json:"zone"`
    SizeGb                       string                      `json:"sizeGb"`
    SourceImageEncryptionKeys    SourceImageEncryptionKey    `json:"sourceImageEncryptionKey"`
    DiskEncryptionKeys           DiskEncryptionKey           `json:"diskEncryptionKey"`
    SourceSnapshotEncryptionKeys SourceSnapshotEncryptionKey `json:"sourceSnapshotEncryptionKey"`
    Licenses                     []string                    `json:"licenses"`
    Users                        []string                    `json:"users"`

    CreationTimestamp   string `json:"creationTimestamp"`
    Description         string `json:"description"`
    ID                  string `json:"id"`
    Kind                string `json:"kind"`
    LabelFingerprint    string `json:"labelFingerprint"`
    SourceSnapshotID    string `json:"sourceSnapshotId"`
    Status              string `json:"status"`
    LastAttachTimestamp string `json:"lastAttachTimestamp"`
    LastDetachTimestamp string `json:"lastDetachTimestamp"`
    Options             string `json:"options"`
    SelfLink            string `json:"selfLink"`
    SourceImage         string `json:"sourceImage"`
    SourceImageID       string `json:"sourceImageId"`
    SourceSnapshot      string `json:"sourceSnapshot"`
}

type DiskEncryptionKey struct {
    RawKey string `json:"rawKey"`
    Sha256 string `json:"sha256"`
}

type GoogleStorage struct {
    Name   string `json:"name"`
    Type   string `json:"type"`
    Zone   string `json:"zone"`
    SizeGb string `json:"sizeGb"`
}

func (googlestorage *GoogleStorage) Attachdisk(request interface{}) (resp interface{}, err error)

func (googlestorage *GoogleStorage) Createdisk(request interface{}) (resp interface{}, err error)

func (googlestorage *GoogleStorage) Createsnapshot(request interface{}) (resp interface{}, err error)

func (googlestorage *GoogleStorage) Deletedisk(request interface{}) (resp interface{}, err error)

func (googlestorage *GoogleStorage) Deletesnapshot(request interface{}) (resp interface{}, err error)

func (googlestorage *GoogleStorage) Detachdisk(request interface{}) (resp interface{}, err error)

type InitializeParams struct {
    DiskName                  string                   `json:"diskName"`
    DiskType                  string                   `json:"diskType"`
    DiskSizeGb                string                   `json:"diskSizeGb"`
    SourceImage               string                   `json:"sourceImage"`
    SourceImageEncryptionKeys SourceImageEncryptionKey `json:"sourceImageEncryptionKey"`
}

type Snapshot struct {
    Name                     string                  `json:"name"`
    CreationTimestamp        string                  `json:"creationTimestamp"`
    Description              string                  `json:"description"`
    DiskSizeGb               string                  `json:"diskSizeGb"`
    ID                       string                  `json:"id"`
    Kind                     string                  `json:"kind"`
    LabelFingerprint         string                  `json:"labelFingerprint"`
    SelfLink                 string                  `json:"selfLink"`
    SourceDisk               string                  `json:"sourceDisk"`
    SourceDiskID             string                  `json:"sourceDiskId"`
    Status                   string                  `json:"status"`
    StorageBytes             string                  `json:"storageBytes"`
    StorageBytesStatus       string                  `json:"storageBytesStatus"`
    Licenses                 []string                `json:"licenses"`
    SourceDiskEncryptionKeys SourceDiskEncryptionKey `json:"sourceDiskEncryptionKey"`
    SnapshotEncryptionKeys   SnapshotEncryptionKey   `json:"snapshotEncryptionKey"`
}

type SnapshotEncryptionKey struct {
    RawKey string `json:"rawKey"`
    Sha256 string `json:"sha256"`
}

type SourceDiskEncryptionKey struct {
    RawKey string `json:"rawKey"`
    Sha256 string `json:"sha256"`
}

type SourceImageEncryptionKey struct {
    RawKey string `json:"rawKey"`
    Sha256 string `json:"sha256"`
}

type SourceSnapshotEncryptionKey struct {
    RawKey string `json:"rawKey"`
    Sha256 string `json:"sha256"`
}


