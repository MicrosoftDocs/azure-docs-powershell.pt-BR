---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945520"
---
# <span data-ttu-id="6daac-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="6daac-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="6daac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6daac-102">SYNOPSIS</span></span>
<span data-ttu-id="6daac-103">Cria um contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-103">Creates a volume container.</span></span>

## <span data-ttu-id="6daac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6daac-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6daac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6daac-105">DESCRIPTION</span></span>
<span data-ttu-id="6daac-106">O cmdlet **New-AzureStorSimpleDeviceVolumeContainer** cria um contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="6daac-107">Você deve associar uma credencial de conta de armazenamento ao novo contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="6daac-108">Para obter uma credencial de conta de armazenamento, use o cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="6daac-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="6daac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6daac-109">EXAMPLES</span></span>

### <span data-ttu-id="6daac-110">Exemplo 1: criar um contêiner</span><span class="sxs-lookup"><span data-stu-id="6daac-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="6daac-111">Esse comando obtém a credencial da conta de armazenamento da conta chamada ContosoAccount usando o cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="6daac-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="6daac-112">O comando passa a credencial para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6daac-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6daac-113">Esse cmdlet usa a credencial desse cmdlet para criar o contêiner chamado Container08 no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="6daac-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="6daac-114">Esse comando inicia o trabalho e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="6daac-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="6daac-115">Para ver o status do trabalho, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="6daac-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="6daac-116">OS</span><span class="sxs-lookup"><span data-stu-id="6daac-116">PARAMETERS</span></span>

### <span data-ttu-id="6daac-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="6daac-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="6daac-118">Especifica a taxa de largura de banda em megabits por segundo (Mbps).</span><span class="sxs-lookup"><span data-stu-id="6daac-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6daac-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6daac-119">-DeviceName</span></span>
<span data-ttu-id="6daac-120">Especifica o nome do dispositivo StorSimple no qual criar o contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6daac-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="6daac-121">-EncryptionEnabled</span></span>
<span data-ttu-id="6daac-122">Indica se a criptografia deve ser ativada.</span><span class="sxs-lookup"><span data-stu-id="6daac-122">Indicates whether to enable encryption.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6daac-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6daac-123">-EncryptionKey</span></span>
<span data-ttu-id="6daac-124">Especifica a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6daac-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="6daac-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6daac-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="6daac-126">Especifica a credencial, como um objeto **StorageAccountCredential** , para associar ao novo contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="6daac-127">Para obter um objeto **StorageAccountCredential** , use o cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="6daac-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6daac-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6daac-128">-Profile</span></span>
<span data-ttu-id="6daac-129">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="6daac-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6daac-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="6daac-130">-VolumeContainerName</span></span>
<span data-ttu-id="6daac-131">Especifica o nome do contêiner de volume a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6daac-131">Specifies the name of the volume container to create.</span></span>

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

### <span data-ttu-id="6daac-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6daac-132">-WaitForComplete</span></span>
<span data-ttu-id="6daac-133">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6daac-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="6daac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6daac-134">CommonParameters</span></span>
<span data-ttu-id="6daac-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6daac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6daac-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6daac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6daac-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6daac-137">INPUTS</span></span>

### <span data-ttu-id="6daac-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6daac-138">StorageAccountCredential</span></span>
<span data-ttu-id="6daac-139">Esse cmdlet aceita um objeto **PrimaryStorageAccountCredential** para associar ao contêiner de volume.</span><span class="sxs-lookup"><span data-stu-id="6daac-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="6daac-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6daac-140">OUTPUTS</span></span>

### <span data-ttu-id="6daac-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="6daac-141">TaskStatusInfo</span></span>
<span data-ttu-id="6daac-142">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="6daac-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="6daac-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6daac-143">NOTES</span></span>

## <span data-ttu-id="6daac-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6daac-144">RELATED LINKS</span></span>

[<span data-ttu-id="6daac-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="6daac-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="6daac-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="6daac-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="6daac-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6daac-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="6daac-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6daac-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


