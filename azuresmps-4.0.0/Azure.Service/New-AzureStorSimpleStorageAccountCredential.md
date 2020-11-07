---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945513"
---
# <span data-ttu-id="9c764-101">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c764-101">New-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="9c764-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c764-102">SYNOPSIS</span></span>
<span data-ttu-id="9c764-103">Adiciona uma credencial de acesso de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c764-103">Adds an Azure storage access credential.</span></span>

## <span data-ttu-id="9c764-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c764-104">SYNTAX</span></span>

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c764-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c764-105">DESCRIPTION</span></span>
<span data-ttu-id="9c764-106">O cmdlet **New-AzureStorSimpleStorageAccountCredential** adiciona uma credencial de acesso de armazenamento do Azure ao StorSimple Manager para uso por cmdlets do storsimple OneSDK.</span><span class="sxs-lookup"><span data-stu-id="9c764-106">The **New-AzureStorSimpleStorageAccountCredential** cmdlet adds an Azure storage access credential to StorSimple manager for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="9c764-107">A maioria dos cmdlets do StorSimple OneSDK lida com entidades que, por fim, estão associadas a uma conta de armazenamento específica, como volumes, contêineres de volume, backups e políticas de backup.</span><span class="sxs-lookup"><span data-stu-id="9c764-107">Most of the StorSimple OneSDK cmdlets deal with entities that are eventually tied to a specific storage account, such as volumes, volume containers, backups, and backup policies.</span></span>
<span data-ttu-id="9c764-108">Para alguns cmdlets, você deve fornecer as credenciais da conta de armazenamento em uso.</span><span class="sxs-lookup"><span data-stu-id="9c764-108">For some cmdlets, you must provide the credentials of the storage account in use.</span></span>
<span data-ttu-id="9c764-109">Uma credencial de conta de armazenamento é um objeto do Access criado no OneSDK que aponta para uma conta de armazenamento existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c764-109">A storage account credential is an access object created in OneSDK that points to an existing Azure storage account.</span></span>
<span data-ttu-id="9c764-110">Você fornece o nome e a chave de acesso de uma conta de armazenamento existente para criar uma credencial de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c764-110">You provide the name and access key of an existing storage account to create a storage account credential.</span></span>
<span data-ttu-id="9c764-111">Em seguida, você pode usar esse objeto de credenciais com outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9c764-111">You can then use that credential object with other cmdlets.</span></span>

<span data-ttu-id="9c764-112">Esse cmdlet usa a chave de registro fornecida quando você seleciona o recurso usando o cmdlet **Select-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="9c764-112">This cmdlet uses the registration key that you provide when you select the resource by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>
<span data-ttu-id="9c764-113">Certifique-se de que o valor está correto para evitar falha na criptografia.</span><span class="sxs-lookup"><span data-stu-id="9c764-113">Be sure that value is correct to avoid encryption failure.</span></span>
<span data-ttu-id="9c764-114">Para modificar a chave de registro para um valor correto, use **Select-AzureStorSimpleResource**.</span><span class="sxs-lookup"><span data-stu-id="9c764-114">To modify the registration key to a correct value, use **Select-AzureStorSimpleResource**.</span></span>

## <span data-ttu-id="9c764-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c764-115">EXAMPLES</span></span>

### <span data-ttu-id="9c764-116">Exemplo 1: criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="9c764-116">Example 1: Create a credential</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="9c764-117">Esse comando cria uma credencial de acesso de armazenamento para a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="9c764-117">This command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="9c764-118">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o cmdlet aguarda até que a tarefa termine para retornar o controle ao console.</span><span class="sxs-lookup"><span data-stu-id="9c764-118">This command specifies the *WaitForComplete* parameter, and, so, the cmdlet waits until the task finishes to return control to the console.</span></span>

### <span data-ttu-id="9c764-119">Exemplo 2: criar uma credencial e consultar o status da tarefa</span><span class="sxs-lookup"><span data-stu-id="9c764-119">Example 2: Create a credential and query that status of the task</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

<span data-ttu-id="9c764-120">O primeiro comando cria uma credencial de acesso de armazenamento para a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="9c764-120">The first command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="9c764-121">O comando retorna uma ID de tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c764-121">The command returns a task ID.</span></span>

<span data-ttu-id="9c764-122">O segundo comando consulta o status da tarefa usando o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="9c764-122">The second command queries the status of the task by using the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="9c764-123">O comando especifica a identificação da tarefa do primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="9c764-123">The command specifies the task ID from the first command.</span></span>

### <span data-ttu-id="9c764-124">Exemplo 3: criar uma credencial para usar com outro cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c764-124">Example 3: Create a credential to use with another cmdlet</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="9c764-125">Esse comando cria uma credencial de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c764-125">This command creates a storage account credential.</span></span>
<span data-ttu-id="9c764-126">Em seguida, o comando passa essa credencial para o cmdlet **New-AzureStorSimpleDeviceVolumeContainer** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c764-126">The command then passes that credential to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c764-127">Esse cmdlet cria um novo contêiner de volume usando a credencial.</span><span class="sxs-lookup"><span data-stu-id="9c764-127">That cmdlet creates a new volume container by using the credential.</span></span>

## <span data-ttu-id="9c764-128">OS</span><span class="sxs-lookup"><span data-stu-id="9c764-128">PARAMETERS</span></span>

### <span data-ttu-id="9c764-129">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9c764-129">-Endpoint</span></span>
<span data-ttu-id="9c764-130">Especifica o ponto de extremidade de armazenamento do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c764-130">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="9c764-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9c764-131">-Profile</span></span>
<span data-ttu-id="9c764-132">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c764-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9c764-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9c764-133">-StorageAccountKey</span></span>
<span data-ttu-id="9c764-134">Especifica a tecla de acesso da conta de armazenamento em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="9c764-134">Specifies the access key of the storage account in plain text.</span></span>

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

### <span data-ttu-id="9c764-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9c764-135">-StorageAccountName</span></span>
<span data-ttu-id="9c764-136">Especifica o nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="9c764-136">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="9c764-137">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="9c764-137">-UseSSL</span></span>
<span data-ttu-id="9c764-138">Indica se você deve usar SSL para a conexão ao usar a nova credencial de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c764-138">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c764-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9c764-139">-WaitForComplete</span></span>
<span data-ttu-id="9c764-140">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9c764-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c764-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c764-141">CommonParameters</span></span>
<span data-ttu-id="9c764-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c764-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c764-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c764-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c764-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c764-144">INPUTS</span></span>

### <span data-ttu-id="9c764-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c764-145">None</span></span>

## <span data-ttu-id="9c764-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c764-146">OUTPUTS</span></span>

### <span data-ttu-id="9c764-147">IEnumerable \<StorageAccountCredentialResponse\> , TaskResponse</span><span class="sxs-lookup"><span data-stu-id="9c764-147">IEnumerable\<StorageAccountCredentialResponse\>, TaskResponse</span></span>
<span data-ttu-id="9c764-148">Esse cmdlet retorna uma lista de objetos **StorageAccountCredentialResponse** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="9c764-148">This cmdlet returns a list of **StorageAccountCredentialResponse** objects, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="9c764-149">Se você não especificar esse parâmetro, o cmdlet retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="9c764-149">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="9c764-150">Um **StorageAccountCredentialResponse** contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="9c764-150">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="9c764-151">**Cloudtype** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="9c764-151">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="9c764-152">**Nome do host** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="9c764-152">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="9c764-153">**InstanceId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="9c764-153">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="9c764-154">**IsDefault** ( **Boolean** )</span><span class="sxs-lookup"><span data-stu-id="9c764-154">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="9c764-155">**Local** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="9c764-155">**Location** ( **String** )</span></span>
- <span data-ttu-id="9c764-156">**Login** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="9c764-156">**Login** ( **String** )</span></span>
- <span data-ttu-id="9c764-157">**Name** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="9c764-157">**Name** ( **String** )</span></span>
- <span data-ttu-id="9c764-158">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="9c764-158">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="9c764-159">**Senha** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="9c764-159">**Password** ( **String** )</span></span>
- <span data-ttu-id="9c764-160">**PasswordEncryptionCertThumbprint** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="9c764-160">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="9c764-161">**UseSSL** ( **booliano** )</span><span class="sxs-lookup"><span data-stu-id="9c764-161">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="9c764-162">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="9c764-162">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="9c764-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c764-163">NOTES</span></span>

## <span data-ttu-id="9c764-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c764-164">RELATED LINKS</span></span>

[<span data-ttu-id="9c764-165">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c764-165">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="9c764-166">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c764-166">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="9c764-167">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c764-167">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="9c764-168">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="9c764-168">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="9c764-169">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9c764-169">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


