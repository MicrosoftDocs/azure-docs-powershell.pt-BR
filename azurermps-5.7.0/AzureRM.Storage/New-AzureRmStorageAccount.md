---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433360"
---
# <span data-ttu-id="3dcb2-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3dcb2-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="3dcb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dcb2-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcb2-103">Cria uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dcb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dcb2-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3dcb2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3dcb2-105">DESCRIPTION</span></span>
<span data-ttu-id="3dcb2-106">O cmdlet **New-AzureRmStorageAccount** cria uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="3dcb2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dcb2-107">EXAMPLES</span></span>

### <span data-ttu-id="3dcb2-108">Exemplo 1: criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3dcb2-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="3dcb2-109">Esse comando cria uma conta de armazenamento para o nome do grupo de recursos MyResource.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="3dcb2-110">Exemplo 2: criar uma conta de armazenamento BLOB que usa criptografia de serviço de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3dcb2-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="3dcb2-111">Esse comando cria uma conta de armazenamento BLOB que usa o tipo de acesso dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="3dcb2-112">A conta habilitou a criptografia do serviço de armazenamento no serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="3dcb2-113">Exemplo 3: criar uma conta de armazenamento que habilite a criptografia do serviço de armazenamento no BLOB e em serviços de arquivo e gere e atribua uma identidade para o repositório de senhas do Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="3dcb2-114">Esse comando cria uma conta de armazenamento que habilitou a criptografia do serviço de armazenamento no BLOB e nos serviços de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="3dcb2-115">Ele também gera e atribui uma identidade que pode ser usada para gerenciar as chaves de conta por meio do Azure keyvault.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="3dcb2-116">OS</span><span class="sxs-lookup"><span data-stu-id="3dcb2-116">PARAMETERS</span></span>

### <span data-ttu-id="3dcb2-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="3dcb2-117">-AccessTier</span></span>
<span data-ttu-id="3dcb2-118">Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="3dcb2-119">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="3dcb2-120">Se você especificar um valor de BlobStorage para o parâmetro *Kind* , você deve especificar um valor para o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3dcb2-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="3dcb2-121">Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3dcb2-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3dcb2-122">-AssignIdentity</span></span>
<span data-ttu-id="3dcb2-123">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3dcb2-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3dcb2-124">-CustomDomainName</span></span>
<span data-ttu-id="3dcb2-125">Especifica o nome do domínio personalizado da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="3dcb2-126">O valor padrão é armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="3dcb2-127">-EnableEncryptionService</span></span>
<span data-ttu-id="3dcb2-128">Indica se esse cmdlet habilita a criptografia do serviço de armazenamento no serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="3dcb2-129">O Azure Blob e o Azure File Services são suportados.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="3dcb2-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="3dcb2-131">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-132">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3dcb2-132">-InformationAction</span></span>
<span data-ttu-id="3dcb2-133">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3dcb2-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3dcb2-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dcb2-135">Contínuo</span><span class="sxs-lookup"><span data-stu-id="3dcb2-135">Continue</span></span>
- <span data-ttu-id="3dcb2-136">Ignorar</span><span class="sxs-lookup"><span data-stu-id="3dcb2-136">Ignore</span></span>
- <span data-ttu-id="3dcb2-137">Inquire</span><span class="sxs-lookup"><span data-stu-id="3dcb2-137">Inquire</span></span>
- <span data-ttu-id="3dcb2-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3dcb2-138">SilentlyContinue</span></span>
- <span data-ttu-id="3dcb2-139">Finaliza</span><span class="sxs-lookup"><span data-stu-id="3dcb2-139">Stop</span></span>
- <span data-ttu-id="3dcb2-140">Suspensão</span><span class="sxs-lookup"><span data-stu-id="3dcb2-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3dcb2-141">-InformationVariable</span></span>
<span data-ttu-id="3dcb2-142">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-143">-Kind</span><span class="sxs-lookup"><span data-stu-id="3dcb2-143">-Kind</span></span>
<span data-ttu-id="3dcb2-144">Especifica o tipo de conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="3dcb2-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3dcb2-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dcb2-146">SPS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-146">Storage.</span></span>
<span data-ttu-id="3dcb2-147">Conta de armazenamento de finalidade geral que dá suporte ao armazenamento de BLOBs, tabelas, filas, arquivos e discos.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="3dcb2-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-148">BlobStorage.</span></span>
<span data-ttu-id="3dcb2-149">Conta de armazenamento de BLOB que dá suporte somente ao armazenamento de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="3dcb2-150">O valor padrão é armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-151">-Local</span><span class="sxs-lookup"><span data-stu-id="3dcb2-151">-Location</span></span>
<span data-ttu-id="3dcb2-152">Especifica o local da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dcb2-153">-Name</span></span>
<span data-ttu-id="3dcb2-154">Especifica o nome da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dcb2-155">-ResourceGroupName</span></span>
<span data-ttu-id="3dcb2-156">Especifica o nome do grupo de recursos no qual a conta de armazenamento será adicionada.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3dcb2-157">-SkuName</span></span>
<span data-ttu-id="3dcb2-158">Especifica o nome do SKU da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="3dcb2-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3dcb2-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dcb2-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-160">Standard_LRS.</span></span>
<span data-ttu-id="3dcb2-161">Armazenamento redundante localmente.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="3dcb2-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-162">Standard_ZRS.</span></span>
<span data-ttu-id="3dcb2-163">Armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="3dcb2-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-164">Standard_GRS.</span></span>
<span data-ttu-id="3dcb2-165">Armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="3dcb2-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-166">Standard_RAGRS.</span></span>
<span data-ttu-id="3dcb2-167">Acesso de leitura com armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="3dcb2-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-168">Premium_LRS.</span></span>
<span data-ttu-id="3dcb2-169">Premium-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-170">-Marca</span><span class="sxs-lookup"><span data-stu-id="3dcb2-170">-Tag</span></span>
<span data-ttu-id="3dcb2-171">Se você especificar um valor de BlobStorage para o parâmetro *Kind* , você deve especificar um valor para o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3dcb2-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="3dcb2-172">Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3dcb2-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-173">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="3dcb2-173">-UseSubDomain</span></span>
<span data-ttu-id="3dcb2-174">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcb2-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcb2-175">CommonParameters</span></span>
<span data-ttu-id="3dcb2-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcb2-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dcb2-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcb2-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3dcb2-178">INPUTS</span></span>

### <span data-ttu-id="3dcb2-179">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3dcb2-179">None</span></span>
<span data-ttu-id="3dcb2-180">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3dcb2-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3dcb2-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3dcb2-181">OUTPUTS</span></span>

## <span data-ttu-id="3dcb2-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3dcb2-182">NOTES</span></span>

## <span data-ttu-id="3dcb2-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dcb2-183">RELATED LINKS</span></span>

[<span data-ttu-id="3dcb2-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3dcb2-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="3dcb2-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3dcb2-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="3dcb2-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3dcb2-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
