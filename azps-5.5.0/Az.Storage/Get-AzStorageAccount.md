---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113672"
---
# <span data-ttu-id="2b630-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b630-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="2b630-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b630-102">SYNOPSIS</span></span>
<span data-ttu-id="2b630-103">Obtém uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b630-103">Gets a Storage account.</span></span>

## <span data-ttu-id="2b630-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b630-104">SYNTAX</span></span>

### <span data-ttu-id="2b630-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b630-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b630-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b630-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b630-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b630-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b630-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b630-108">DESCRIPTION</span></span>
<span data-ttu-id="2b630-109">O cmdlet **Get-AzStorageAccount** obtém uma conta de Armazenamento especificada ou todas as contas de Armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b630-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="2b630-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b630-110">EXAMPLES</span></span>

### <span data-ttu-id="2b630-111">Exemplo 1: Obter uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="2b630-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="2b630-112">Esse comando obtém a conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="2b630-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="2b630-113">Exemplo 2: Obter todas as contas de Armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2b630-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="2b630-114">Esse comando obtém todas as contas de Armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b630-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="2b630-115">Exemplo 3: Obter todas as contas de Armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="2b630-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="2b630-116">Esse comando obtém todas as contas de Armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b630-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="2b630-117">Exemplo 4: Obter uma conta de armazenamento com seu status de restauração de blob</span><span class="sxs-lookup"><span data-stu-id="2b630-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="2b630-118">Esse comando obtém uma conta de Armazenamento com seu status de restauração de blob e mostra o status de restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="2b630-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="2b630-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b630-119">PARAMETERS</span></span>

### <span data-ttu-id="2b630-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b630-120">-AsJob</span></span>
<span data-ttu-id="2b630-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2b630-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b630-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b630-122">-DefaultProfile</span></span>
<span data-ttu-id="2b630-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b630-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b630-124">-IncludeBstoreStatus</span><span class="sxs-lookup"><span data-stu-id="2b630-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="2b630-125">Obter o BlobRestoreStatus da conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b630-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="2b630-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="2b630-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="2b630-127">Obter os GeoReplicationStats da conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b630-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="2b630-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b630-128">-Name</span></span>
<span data-ttu-id="2b630-129">Especifica o nome da conta de armazenamento a ser obter.</span><span class="sxs-lookup"><span data-stu-id="2b630-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="2b630-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b630-130">-ResourceGroupName</span></span>
<span data-ttu-id="2b630-131">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obter.</span><span class="sxs-lookup"><span data-stu-id="2b630-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="2b630-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b630-132">CommonParameters</span></span>
<span data-ttu-id="2b630-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b630-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b630-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b630-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b630-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b630-135">INPUTS</span></span>

### <span data-ttu-id="2b630-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2b630-136">System.String</span></span>

## <span data-ttu-id="2b630-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b630-137">OUTPUTS</span></span>

### <span data-ttu-id="2b630-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b630-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2b630-139">Notas</span><span class="sxs-lookup"><span data-stu-id="2b630-139">NOTES</span></span>

## <span data-ttu-id="2b630-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b630-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b630-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b630-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="2b630-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b630-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="2b630-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b630-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


