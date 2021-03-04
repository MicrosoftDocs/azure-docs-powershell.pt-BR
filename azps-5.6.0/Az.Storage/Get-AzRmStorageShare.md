---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892005"
---
# <span data-ttu-id="9d77e-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9d77e-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="9d77e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d77e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d77e-103">Obtém ou lista compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="9d77e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9d77e-104">SYNTAX</span></span>

### <span data-ttu-id="9d77e-105">AccountNameSingle (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9d77e-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d77e-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="9d77e-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d77e-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="9d77e-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d77e-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9d77e-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d77e-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="9d77e-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d77e-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9d77e-110">DESCRIPTION</span></span>
<span data-ttu-id="9d77e-111">O cmdlet **Get-AzRmStorageShare** obtém ou lista compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="9d77e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d77e-112">EXAMPLES</span></span>

### <span data-ttu-id="9d77e-113">Exemplo 1: Obter um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9d77e-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="9d77e-114">Este comando obtém um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="9d77e-115">Exemplo 2: Listar todos os compartilhamentos de arquivo de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9d77e-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="9d77e-116">Este comando lista todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="9d77e-117">Exemplo 3: Obter um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9d77e-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="9d77e-118">Este comando obtém um contêiner blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9d77e-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9d77e-119">Exemplo 4: Obter um compartilhamento de arquivos de armazenamento com o uso de compartilhamento em bytes</span><span class="sxs-lookup"><span data-stu-id="9d77e-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="9d77e-120">Este comando obtém um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento e inclui o uso do compartilhamento em bytes.</span><span class="sxs-lookup"><span data-stu-id="9d77e-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="9d77e-121">Exemplo 5: listar todos os compartilhamentos de arquivo de armazenamento de uma conta de armazenamento, inclua os compartilhamentos excluídos</span><span class="sxs-lookup"><span data-stu-id="9d77e-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="9d77e-122">Este comando lista todos os compartilhamentos de arquivo de armazenamento que incluem os compartilhamentos excluídos de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="9d77e-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9d77e-123">PARAMETERS</span></span>

### <span data-ttu-id="9d77e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d77e-124">-DefaultProfile</span></span>
<span data-ttu-id="9d77e-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d77e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d77e-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="9d77e-126">-GetShareUsage</span></span>
<span data-ttu-id="9d77e-127">Especifique esse parâmetro para obter o Uso do Compartilhamento em Bytes.</span><span class="sxs-lookup"><span data-stu-id="9d77e-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="9d77e-128">-IncludeDeleted</span></span>
<span data-ttu-id="9d77e-129">Incluir compartilhamentos excluídos, por padrão, os compartilhamentos de lista não incluirão compartilhamentos excluídos</span><span class="sxs-lookup"><span data-stu-id="9d77e-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9d77e-130">-Name</span></span>
<span data-ttu-id="9d77e-131">Nome do Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9d77e-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d77e-132">-ResourceGroupName</span></span>
<span data-ttu-id="9d77e-133">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="9d77e-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d77e-134">-ResourceId</span></span>
<span data-ttu-id="9d77e-135">Entrada de uma ID de Recurso de Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d77e-135">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d77e-136">-StorageAccount</span></span>
<span data-ttu-id="9d77e-137">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9d77e-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d77e-138">-StorageAccountName</span></span>
<span data-ttu-id="9d77e-139">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d77e-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d77e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d77e-140">CommonParameters</span></span>
<span data-ttu-id="9d77e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d77e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d77e-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d77e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d77e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d77e-143">INPUTS</span></span>

### <span data-ttu-id="9d77e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9d77e-144">System.String</span></span>

### <span data-ttu-id="9d77e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d77e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9d77e-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9d77e-146">OUTPUTS</span></span>

### <span data-ttu-id="9d77e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="9d77e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="9d77e-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="9d77e-148">NOTES</span></span>

## <span data-ttu-id="9d77e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d77e-149">RELATED LINKS</span></span>
