---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945517"
---
# <span data-ttu-id="9827a-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9827a-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="9827a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9827a-102">SYNOPSIS</span></span>
<span data-ttu-id="9827a-103">Cria uma credencial de conta de armazenamento embutido.</span><span class="sxs-lookup"><span data-stu-id="9827a-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="9827a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9827a-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9827a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9827a-105">DESCRIPTION</span></span>
<span data-ttu-id="9827a-106">O cmdlet **New-AzureStorSimpleInlineStorageAccountCredential** cria um objeto de credencial de conta de armazenamento embutido do Azure.</span><span class="sxs-lookup"><span data-stu-id="9827a-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="9827a-107">Esse cmdlet cria um objeto de credencial fictício.</span><span class="sxs-lookup"><span data-stu-id="9827a-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="9827a-108">Você pode usar o cmdlet **New-AzureStorSimpleDeviceVolumeContainer** e o cmdlet atual no mesmo comando usando o pipeline do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9827a-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="9827a-109">O objeto de credencial da conta de armazenamento real é criado como parte da criação do contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="9827a-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="9827a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9827a-110">EXAMPLES</span></span>

### <span data-ttu-id="9827a-111">Exemplo 1: criar uma credencial de conta de armazenamento embutida</span><span class="sxs-lookup"><span data-stu-id="9827a-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="9827a-112">Esse comando cria uma credencial de conta de armazenamento embutida e, em seguida, a transmite para o cmdlet **New-AzureStorSimpleDeviceVolumeContainer** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="9827a-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9827a-113">Esse contêiner usa a credencial fictícia para criar um contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="9827a-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="9827a-114">OS</span><span class="sxs-lookup"><span data-stu-id="9827a-114">PARAMETERS</span></span>

### <span data-ttu-id="9827a-115">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9827a-115">-Endpoint</span></span>
<span data-ttu-id="9827a-116">Especifica o ponto de extremidade de armazenamento do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9827a-116">Specifies the Azure storage endpoint for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9827a-117">-Profile</span></span>
<span data-ttu-id="9827a-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9827a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9827a-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9827a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9827a-120">-StorageAccountKey</span></span>
<span data-ttu-id="9827a-121">Especifica a chave da conta de armazenamento em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="9827a-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="9827a-122">A chave é transferida em formato criptografado.</span><span class="sxs-lookup"><span data-stu-id="9827a-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9827a-123">-StorageAccountName</span></span>
<span data-ttu-id="9827a-124">Especifica o nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="9827a-124">Specifies the name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9827a-125">CommonParameters</span></span>
<span data-ttu-id="9827a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9827a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9827a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9827a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9827a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9827a-128">INPUTS</span></span>

### <span data-ttu-id="9827a-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9827a-129">None</span></span>

## <span data-ttu-id="9827a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9827a-130">OUTPUTS</span></span>

### <span data-ttu-id="9827a-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="9827a-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="9827a-132">Esse cmdlet retorna um objeto **cloudtype** , que contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="9827a-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="9827a-133">**Nome do host**.</span><span class="sxs-lookup"><span data-stu-id="9827a-133">**Hostname**.</span></span>
<span data-ttu-id="9827a-134">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-134">**String**.</span></span> 
- <span data-ttu-id="9827a-135">**InstanceId**.</span><span class="sxs-lookup"><span data-stu-id="9827a-135">**InstanceId**.</span></span>
<span data-ttu-id="9827a-136">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-136">**String**.</span></span> 
- <span data-ttu-id="9827a-137">**IsDefault**.</span><span class="sxs-lookup"><span data-stu-id="9827a-137">**IsDefault**.</span></span>
<span data-ttu-id="9827a-138">**Booliano**.</span><span class="sxs-lookup"><span data-stu-id="9827a-138">**Boolean**.</span></span> 
- <span data-ttu-id="9827a-139">**Local**.</span><span class="sxs-lookup"><span data-stu-id="9827a-139">**Location**.</span></span>
<span data-ttu-id="9827a-140">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-140">**String**.</span></span> 
- <span data-ttu-id="9827a-141">**Logon**.</span><span class="sxs-lookup"><span data-stu-id="9827a-141">**Login**.</span></span>
<span data-ttu-id="9827a-142">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-142">**String**.</span></span> 
- <span data-ttu-id="9827a-143">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="9827a-143">**Name**.</span></span>
<span data-ttu-id="9827a-144">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-144">**String**.</span></span> 
- <span data-ttu-id="9827a-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="9827a-145">**OperationInProgress**.</span></span>
<span data-ttu-id="9827a-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="9827a-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="9827a-147">**Senha**.</span><span class="sxs-lookup"><span data-stu-id="9827a-147">**Password**.</span></span>
<span data-ttu-id="9827a-148">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-148">**String**.</span></span> 
- <span data-ttu-id="9827a-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="9827a-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="9827a-150">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9827a-150">**String**.</span></span> 
- <span data-ttu-id="9827a-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="9827a-151">**UseSSL**.</span></span>
<span data-ttu-id="9827a-152">**Booliano**.</span><span class="sxs-lookup"><span data-stu-id="9827a-152">**Boolean**.</span></span> 
- <span data-ttu-id="9827a-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="9827a-153">**VolumeCount**.</span></span>
<span data-ttu-id="9827a-154">**Número inteiro**.</span><span class="sxs-lookup"><span data-stu-id="9827a-154">**Integer**.</span></span>

## <span data-ttu-id="9827a-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9827a-155">NOTES</span></span>

## <span data-ttu-id="9827a-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9827a-156">RELATED LINKS</span></span>

[<span data-ttu-id="9827a-157">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9827a-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="9827a-158">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9827a-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


