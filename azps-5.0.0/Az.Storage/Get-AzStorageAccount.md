---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125705"
---
# <span data-ttu-id="c8f83-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f83-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="c8f83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8f83-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f83-103">Obtém uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8f83-103">Gets a Storage account.</span></span>

## <span data-ttu-id="c8f83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8f83-104">SYNTAX</span></span>

### <span data-ttu-id="c8f83-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f83-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8f83-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f83-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8f83-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f83-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8f83-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8f83-108">DESCRIPTION</span></span>
<span data-ttu-id="c8f83-109">O cmdlet **Get-AzStorageAccount** Obtém uma conta de armazenamento especificada ou todas as contas de armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8f83-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="c8f83-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8f83-110">EXAMPLES</span></span>

### <span data-ttu-id="c8f83-111">Exemplo 1: obter uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="c8f83-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="c8f83-112">Este comando obtém a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="c8f83-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="c8f83-113">Exemplo 2: obter todas as contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c8f83-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="c8f83-114">Este comando obtém todas as contas de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8f83-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="c8f83-115">Exemplo 3: obter todas as contas de armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="c8f83-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="c8f83-116">Este comando obtém todas as contas de armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8f83-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="c8f83-117">Exemplo 4: obter uma conta de armazenamento com seu status de restauração de BLOB</span><span class="sxs-lookup"><span data-stu-id="c8f83-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="c8f83-118">Esse comando obtém uma conta de armazenamento com seu status de restauração de BLOB e mostra o status da restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="c8f83-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="c8f83-119">OS</span><span class="sxs-lookup"><span data-stu-id="c8f83-119">PARAMETERS</span></span>

### <span data-ttu-id="c8f83-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8f83-120">-AsJob</span></span>
<span data-ttu-id="c8f83-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8f83-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8f83-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f83-122">-DefaultProfile</span></span>
<span data-ttu-id="c8f83-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f83-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f83-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c8f83-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="c8f83-125">Obtenha o BlobRestoreStatus da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8f83-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="c8f83-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="c8f83-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="c8f83-127">Obtenha o GeoReplicationStats da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8f83-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="c8f83-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8f83-128">-Name</span></span>
<span data-ttu-id="c8f83-129">Especifica o nome da conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c8f83-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="c8f83-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f83-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8f83-131">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c8f83-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="c8f83-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f83-132">CommonParameters</span></span>
<span data-ttu-id="c8f83-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f83-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f83-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f83-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f83-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8f83-135">INPUTS</span></span>

### <span data-ttu-id="c8f83-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c8f83-136">System.String</span></span>

## <span data-ttu-id="c8f83-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8f83-137">OUTPUTS</span></span>

### <span data-ttu-id="c8f83-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f83-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c8f83-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8f83-139">NOTES</span></span>

## <span data-ttu-id="c8f83-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8f83-140">RELATED LINKS</span></span>

[<span data-ttu-id="c8f83-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f83-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="c8f83-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f83-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="c8f83-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f83-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


