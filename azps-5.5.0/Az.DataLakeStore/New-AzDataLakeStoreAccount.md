---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117722"
---
# <span data-ttu-id="ce576-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="ce576-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce576-102">SYNOPSIS</span></span>
<span data-ttu-id="ce576-103">Cria uma nova conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce576-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ce576-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce576-104">SYNTAX</span></span>

### <span data-ttu-id="ce576-105">UserOrSystemAssignedEncryption (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce576-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce576-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ce576-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce576-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce576-107">DESCRIPTION</span></span>
<span data-ttu-id="ce576-108">O cmdlet **New-AzDataLakeStoreAccount cria** uma nova conta da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce576-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ce576-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce576-109">EXAMPLES</span></span>

### <span data-ttu-id="ce576-110">Exemplo 1: Criar uma conta</span><span class="sxs-lookup"><span data-stu-id="ce576-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="ce576-111">Esse comando cria uma conta da Data Lake Store chamada ContosoADL para o local do Leste dos EUA 2.</span><span class="sxs-lookup"><span data-stu-id="ce576-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="ce576-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce576-112">PARAMETERS</span></span>

### <span data-ttu-id="ce576-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ce576-113">-DefaultGroup</span></span>
<span data-ttu-id="ce576-114">Especifica a ID de objeto do grupo Diretório AzureActive a ser usado como o proprietário do grupo padrão para novos arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="ce576-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="ce576-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce576-115">-DefaultProfile</span></span>
<span data-ttu-id="ce576-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ce576-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce576-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ce576-117">-DisableEncryption</span></span>
<span data-ttu-id="ce576-118">Indica que a conta não terá nenhuma forma de criptografia aplicada a ela.</span><span class="sxs-lookup"><span data-stu-id="ce576-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="ce576-119">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="ce576-119">-Encryption</span></span>
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

### <span data-ttu-id="ce576-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ce576-120">-KeyName</span></span>
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

### <span data-ttu-id="ce576-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ce576-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="ce576-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ce576-122">-KeyVersion</span></span>
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

### <span data-ttu-id="ce576-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ce576-123">-Location</span></span>
<span data-ttu-id="ce576-124">Especifica o local a ser usado para a conta.</span><span class="sxs-lookup"><span data-stu-id="ce576-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="ce576-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ce576-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce576-126">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="ce576-126">East US 2</span></span>

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

### <span data-ttu-id="ce576-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce576-127">-Name</span></span>
<span data-ttu-id="ce576-128">Especifica o nome da conta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ce576-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="ce576-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce576-129">-ResourceGroupName</span></span>
<span data-ttu-id="ce576-130">Especifica o nome do grupo de recursos que contém a conta.</span><span class="sxs-lookup"><span data-stu-id="ce576-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="ce576-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce576-131">-Tag</span></span>
<span data-ttu-id="ce576-132">Especifica marcas como pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="ce576-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ce576-133">Você pode usar marcas para identificar uma conta do Data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce576-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="ce576-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="ce576-134">-Tier</span></span>
<span data-ttu-id="ce576-135">O nível de compromisso desejado para que essa conta seja usada.</span><span class="sxs-lookup"><span data-stu-id="ce576-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ce576-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce576-136">CommonParameters</span></span>
<span data-ttu-id="ce576-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce576-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce576-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce576-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce576-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="ce576-139">INPUTS</span></span>

### <span data-ttu-id="ce576-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ce576-140">System.String</span></span>

### <span data-ttu-id="ce576-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ce576-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ce576-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ce576-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ce576-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce576-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ce576-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ce576-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ce576-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="ce576-145">OUTPUTS</span></span>

### <span data-ttu-id="ce576-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="ce576-147">Notas</span><span class="sxs-lookup"><span data-stu-id="ce576-147">NOTES</span></span>

## <span data-ttu-id="ce576-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce576-148">RELATED LINKS</span></span>

[<span data-ttu-id="ce576-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ce576-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ce576-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ce576-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce576-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


