---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 81e380f6b6d4b1c35a6cff98093dfedf94119a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954531"
---
# <span data-ttu-id="60750-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60750-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="60750-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60750-102">SYNOPSIS</span></span>
<span data-ttu-id="60750-103">Cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60750-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="60750-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60750-104">SYNTAX</span></span>

### <span data-ttu-id="60750-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="60750-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60750-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="60750-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60750-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60750-107">DESCRIPTION</span></span>
<span data-ttu-id="60750-108">O cmdlet **New-AzRmStorageShare** cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60750-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="60750-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60750-109">EXAMPLES</span></span>

### <span data-ttu-id="60750-110">Exemplo 1: criar um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento, com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="60750-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="60750-111">Esse comando cria um compartilhamento de arquivos de armazenamento com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="60750-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="60750-112">Exemplo 2: criar um compartilhamento de arquivos de armazenamento com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60750-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="60750-113">Esse comando cria um compartilhamento de arquivos de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="60750-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="60750-114">OS</span><span class="sxs-lookup"><span data-stu-id="60750-114">PARAMETERS</span></span>

### <span data-ttu-id="60750-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60750-115">-DefaultProfile</span></span>
<span data-ttu-id="60750-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60750-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60750-117">-Metadados</span><span class="sxs-lookup"><span data-stu-id="60750-117">-Metadata</span></span>
<span data-ttu-id="60750-118">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="60750-118">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="60750-119">-Name</span></span>
<span data-ttu-id="60750-120">Nome do compartilhamento de arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="60750-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="60750-121">-QuotaGiB</span></span>
<span data-ttu-id="60750-122">Compartilhe a cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="60750-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60750-123">-ResourceGroupName</span></span>
<span data-ttu-id="60750-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60750-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="60750-125">-StorageAccount</span></span>
<span data-ttu-id="60750-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60750-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60750-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60750-127">-StorageAccountName</span></span>
<span data-ttu-id="60750-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60750-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60750-129">-Confirm</span></span>
<span data-ttu-id="60750-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60750-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60750-131">-WhatIf</span></span>
<span data-ttu-id="60750-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60750-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60750-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60750-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60750-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60750-134">CommonParameters</span></span>
<span data-ttu-id="60750-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60750-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60750-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60750-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60750-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60750-137">INPUTS</span></span>

### <span data-ttu-id="60750-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60750-138">System.String</span></span>

### <span data-ttu-id="60750-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60750-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="60750-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60750-140">OUTPUTS</span></span>

### <span data-ttu-id="60750-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="60750-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="60750-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60750-142">NOTES</span></span>

## <span data-ttu-id="60750-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60750-143">RELATED LINKS</span></span>
