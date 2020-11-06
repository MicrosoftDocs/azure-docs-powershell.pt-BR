---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c9964bfb6d9f701d88a16b8a227aec7c2018a217
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427565"
---
# <span data-ttu-id="1ecd6-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="1ecd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ecd6-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecd6-103">Cria uma nova conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ecd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ecd6-104">SYNTAX</span></span>

### <span data-ttu-id="1ecd6-105">UserOrSystemAssignedEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ecd6-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ecd6-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1ecd6-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecd6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ecd6-107">DESCRIPTION</span></span>
<span data-ttu-id="1ecd6-108">O cmdlet **New-AzureRmDataLakeStoreAccount** cria uma nova conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="1ecd6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ecd6-109">EXAMPLES</span></span>

### <span data-ttu-id="1ecd6-110">Exemplo 1: criar uma conta</span><span class="sxs-lookup"><span data-stu-id="1ecd6-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="1ecd6-111">Esse comando cria uma conta do data Lake Store chamada ContosoADL para o local do leste EUA 2.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="1ecd6-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ecd6-112">PARAMETERS</span></span>

### <span data-ttu-id="1ecd6-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="1ecd6-113">-DefaultGroup</span></span>
<span data-ttu-id="1ecd6-114">Especifica a ID do objeto do grupo de diretório AzureActive para usar como o proprietário padrão do grupo para novos arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecd6-115">-DefaultProfile</span></span>
<span data-ttu-id="1ecd6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1ecd6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1ecd6-117">-DisableEncryption</span></span>
<span data-ttu-id="1ecd6-118">Indica que a conta não terá nenhuma forma de criptografia aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-119">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="1ecd6-119">-Encryption</span></span>
```yaml
Type: EncryptionConfigType
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1ecd6-120">-KeyName</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-121">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="1ecd6-121">-KeyVaultId</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-122">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="1ecd6-122">-KeyVersion</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-123">-Local</span><span class="sxs-lookup"><span data-stu-id="1ecd6-123">-Location</span></span>
<span data-ttu-id="1ecd6-124">Especifica o local a ser usado para a conta.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="1ecd6-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1ecd6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ecd6-126">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="1ecd6-126">East US 2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ecd6-127">-Name</span></span>
<span data-ttu-id="1ecd6-128">Especifica o nome da conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-128">Specifies the name of the account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecd6-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ecd6-130">Especifica o nome do grupo de recursos que contém a conta.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="1ecd6-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="1ecd6-131">-Tag</span></span>
<span data-ttu-id="1ecd6-132">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="1ecd6-133">Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="1ecd6-134">-Tier</span></span>
<span data-ttu-id="1ecd6-135">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecd6-136">CommonParameters</span></span>
<span data-ttu-id="1ecd6-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecd6-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecd6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecd6-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ecd6-139">INPUTS</span></span>

### <span data-ttu-id="1ecd6-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ecd6-140">None</span></span>
<span data-ttu-id="1ecd6-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ecd6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ecd6-142">OUTPUTS</span></span>

### <span data-ttu-id="1ecd6-143">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-143">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="1ecd6-144">Os detalhes da conta criada.</span><span class="sxs-lookup"><span data-stu-id="1ecd6-144">The created account details.</span></span>

## <span data-ttu-id="1ecd6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ecd6-145">NOTES</span></span>

## <span data-ttu-id="1ecd6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ecd6-146">RELATED LINKS</span></span>

[<span data-ttu-id="1ecd6-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1ecd6-148">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-148">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1ecd6-149">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-149">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1ecd6-150">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd6-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


