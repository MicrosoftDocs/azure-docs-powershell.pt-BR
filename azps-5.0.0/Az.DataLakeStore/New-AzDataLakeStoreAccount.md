---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280816"
---
# <span data-ttu-id="dbddc-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="dbddc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbddc-102">SYNOPSIS</span></span>
<span data-ttu-id="dbddc-103">Cria uma nova conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dbddc-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="dbddc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbddc-104">SYNTAX</span></span>

### <span data-ttu-id="dbddc-105">UserOrSystemAssignedEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="dbddc-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbddc-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="dbddc-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbddc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbddc-107">DESCRIPTION</span></span>
<span data-ttu-id="dbddc-108">O cmdlet **New-AzDataLakeStoreAccount** cria uma nova conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dbddc-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="dbddc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbddc-109">EXAMPLES</span></span>

### <span data-ttu-id="dbddc-110">Exemplo 1: criar uma conta</span><span class="sxs-lookup"><span data-stu-id="dbddc-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="dbddc-111">Esse comando cria uma conta do data Lake Store chamada ContosoADL para o local do leste EUA 2.</span><span class="sxs-lookup"><span data-stu-id="dbddc-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="dbddc-112">OS</span><span class="sxs-lookup"><span data-stu-id="dbddc-112">PARAMETERS</span></span>

### <span data-ttu-id="dbddc-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="dbddc-113">-DefaultGroup</span></span>
<span data-ttu-id="dbddc-114">Especifica a ID do objeto do grupo de diretório AzureActive para usar como o proprietário padrão do grupo para novos arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="dbddc-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbddc-115">-DefaultProfile</span></span>
<span data-ttu-id="dbddc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dbddc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="dbddc-117">-DisableEncryption</span></span>
<span data-ttu-id="dbddc-118">Indica que a conta não terá nenhuma forma de criptografia aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="dbddc-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-119">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="dbddc-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dbddc-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-121">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="dbddc-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-122">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="dbddc-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-123">-Local</span><span class="sxs-lookup"><span data-stu-id="dbddc-123">-Location</span></span>
<span data-ttu-id="dbddc-124">Especifica o local a ser usado para a conta.</span><span class="sxs-lookup"><span data-stu-id="dbddc-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="dbddc-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dbddc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbddc-126">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="dbddc-126">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbddc-127">-Name</span></span>
<span data-ttu-id="dbddc-128">Especifica o nome da conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dbddc-128">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbddc-129">-ResourceGroupName</span></span>
<span data-ttu-id="dbddc-130">Especifica o nome do grupo de recursos que contém a conta.</span><span class="sxs-lookup"><span data-stu-id="dbddc-130">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="dbddc-131">-Tag</span></span>
<span data-ttu-id="dbddc-132">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="dbddc-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="dbddc-133">Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbddc-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="dbddc-134">-Tier</span></span>
<span data-ttu-id="dbddc-135">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="dbddc-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbddc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbddc-136">CommonParameters</span></span>
<span data-ttu-id="dbddc-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbddc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbddc-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbddc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbddc-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbddc-139">INPUTS</span></span>

### <span data-ttu-id="dbddc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dbddc-140">System.String</span></span>

### <span data-ttu-id="dbddc-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dbddc-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dbddc-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. EncryptionConfigType, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dbddc-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dbddc-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dbddc-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dbddc-144">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dbddc-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dbddc-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbddc-145">OUTPUTS</span></span>

### <span data-ttu-id="dbddc-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="dbddc-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbddc-147">NOTES</span></span>

## <span data-ttu-id="dbddc-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbddc-148">RELATED LINKS</span></span>

[<span data-ttu-id="dbddc-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbddc-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbddc-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbddc-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


