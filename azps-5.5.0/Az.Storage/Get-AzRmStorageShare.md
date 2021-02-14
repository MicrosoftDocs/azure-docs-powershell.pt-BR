---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111272"
---
# <span data-ttu-id="e825d-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e825d-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="e825d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e825d-102">SYNOPSIS</span></span>
<span data-ttu-id="e825d-103">Obtém ou lista compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="e825d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e825d-104">SYNTAX</span></span>

### <span data-ttu-id="e825d-105">AccountNameSingle (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e825d-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-106">Accountname</span><span class="sxs-lookup"><span data-stu-id="e825d-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="e825d-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e825d-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825d-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="e825d-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e825d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e825d-110">DESCRIPTION</span></span>
<span data-ttu-id="e825d-111">O **cmdlet Get-AzRmStorageShare** obtém ou lista compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="e825d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e825d-112">EXAMPLES</span></span>

### <span data-ttu-id="e825d-113">Exemplo 1: Obter um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e825d-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="e825d-114">Esse comando obtém um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="e825d-115">Exemplo 2: Listar todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e825d-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="e825d-116">Esse comando lista todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="e825d-117">Exemplo 3: Obter um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e825d-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="e825d-118">Esse comando obtém um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e825d-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="e825d-119">Exemplo 4: Obter um compartilhamento de arquivos de armazenamento com o uso de compartilhamento em bytes</span><span class="sxs-lookup"><span data-stu-id="e825d-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="e825d-120">Esse comando obtém um compartilhamento de arquivos de Armazenamento com o nome da conta de armazenamento e o nome do compartilhamento e inclui o uso do compartilhamento em bytes.</span><span class="sxs-lookup"><span data-stu-id="e825d-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="e825d-121">Exemplo 5: Listar todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento, inclua os compartilhamentos excluídos</span><span class="sxs-lookup"><span data-stu-id="e825d-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="e825d-122">Esse comando lista todos os compartilhamentos de arquivos de armazenamento incluindo os compartilhamentos excluídos de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="e825d-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e825d-123">PARAMETERS</span></span>

### <span data-ttu-id="e825d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e825d-124">-DefaultProfile</span></span>
<span data-ttu-id="e825d-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e825d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e825d-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="e825d-126">-GetShareUsage</span></span>
<span data-ttu-id="e825d-127">Especifique este parâmetro para obter o Uso do Compartilhamento em Bytes.</span><span class="sxs-lookup"><span data-stu-id="e825d-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="e825d-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="e825d-128">-IncludeDeleted</span></span>
<span data-ttu-id="e825d-129">Incluir compartilhamentos excluídos, por padrão, os compartilhamentos de lista não incluirão compartilhamentos excluídos</span><span class="sxs-lookup"><span data-stu-id="e825d-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="e825d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e825d-130">-Name</span></span>
<span data-ttu-id="e825d-131">Compartilhar Nome</span><span class="sxs-lookup"><span data-stu-id="e825d-131">Share Name</span></span>

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

### <span data-ttu-id="e825d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e825d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e825d-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e825d-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="e825d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e825d-134">-ResourceId</span></span>
<span data-ttu-id="e825d-135">Inserir uma ID de Recurso de Compartilhamento de Arquivo.</span><span class="sxs-lookup"><span data-stu-id="e825d-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="e825d-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e825d-136">-StorageAccount</span></span>
<span data-ttu-id="e825d-137">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e825d-137">Storage account object</span></span>

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

### <span data-ttu-id="e825d-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e825d-138">-StorageAccountName</span></span>
<span data-ttu-id="e825d-139">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e825d-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="e825d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e825d-140">CommonParameters</span></span>
<span data-ttu-id="e825d-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e825d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e825d-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e825d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e825d-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="e825d-143">INPUTS</span></span>

### <span data-ttu-id="e825d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e825d-144">System.String</span></span>

### <span data-ttu-id="e825d-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e825d-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e825d-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="e825d-146">OUTPUTS</span></span>

### <span data-ttu-id="e825d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="e825d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e825d-148">Notas</span><span class="sxs-lookup"><span data-stu-id="e825d-148">NOTES</span></span>

## <span data-ttu-id="e825d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e825d-149">RELATED LINKS</span></span>
