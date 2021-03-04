---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2c8980f198dc675e12a9b9c6048a4960c1998f9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892003"
---
# <span data-ttu-id="07fe4-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07fe4-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="07fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="07fe4-103">Obtém uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07fe4-103">Gets a Storage account.</span></span>

## <span data-ttu-id="07fe4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07fe4-104">SYNTAX</span></span>

### <span data-ttu-id="07fe4-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="07fe4-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07fe4-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07fe4-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07fe4-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="07fe4-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07fe4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07fe4-108">DESCRIPTION</span></span>
<span data-ttu-id="07fe4-109">O cmdlet **Get-AzStorageAccount** obtém uma conta de Armazenamento especificada ou todas as contas de Armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="07fe4-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="07fe4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07fe4-110">EXAMPLES</span></span>

### <span data-ttu-id="07fe4-111">Exemplo 1: Obter uma conta de Armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="07fe4-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="07fe4-112">Este comando obtém a conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="07fe4-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="07fe4-113">Exemplo 2: Obter todas as contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="07fe4-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="07fe4-114">Este comando obtém todas as contas de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07fe4-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="07fe4-115">Exemplo 3: Obter todas as contas de armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="07fe4-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="07fe4-116">Este comando obtém todas as contas de Armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="07fe4-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="07fe4-117">Exemplo 4: Obter contas de armazenamento com seu status de restauração de blob</span><span class="sxs-lookup"><span data-stu-id="07fe4-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="07fe4-118">Este comando obtém uma conta de Armazenamento com seu status de restauração de blob e mostra o status de restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="07fe4-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="07fe4-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07fe4-119">PARAMETERS</span></span>

### <span data-ttu-id="07fe4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07fe4-120">-AsJob</span></span>
<span data-ttu-id="07fe4-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="07fe4-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fe4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fe4-122">-DefaultProfile</span></span>
<span data-ttu-id="07fe4-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07fe4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07fe4-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="07fe4-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="07fe4-125">Obter o BlobRestoreStatus da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07fe4-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fe4-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="07fe4-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="07fe4-127">Obter os GeoReplicationStats da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07fe4-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fe4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="07fe4-128">-Name</span></span>
<span data-ttu-id="07fe4-129">Especifica o nome da conta de armazenamento a ser obter.</span><span class="sxs-lookup"><span data-stu-id="07fe4-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fe4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fe4-130">-ResourceGroupName</span></span>
<span data-ttu-id="07fe4-131">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obter.</span><span class="sxs-lookup"><span data-stu-id="07fe4-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fe4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fe4-132">CommonParameters</span></span>
<span data-ttu-id="07fe4-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fe4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fe4-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fe4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fe4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07fe4-135">INPUTS</span></span>

### <span data-ttu-id="07fe4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="07fe4-136">System.String</span></span>

## <span data-ttu-id="07fe4-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07fe4-137">OUTPUTS</span></span>

### <span data-ttu-id="07fe4-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07fe4-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="07fe4-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="07fe4-139">NOTES</span></span>

## <span data-ttu-id="07fe4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07fe4-140">RELATED LINKS</span></span>

[<span data-ttu-id="07fe4-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07fe4-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="07fe4-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07fe4-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="07fe4-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07fe4-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


