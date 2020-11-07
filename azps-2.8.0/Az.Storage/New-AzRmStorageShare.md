---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 01871c63d9a734cba88da30032f8b1da21198160
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774150"
---
# <span data-ttu-id="1540c-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1540c-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="1540c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1540c-102">SYNOPSIS</span></span>
<span data-ttu-id="1540c-103">Cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1540c-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="1540c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1540c-104">SYNTAX</span></span>

### <span data-ttu-id="1540c-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1540c-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1540c-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="1540c-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1540c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1540c-107">DESCRIPTION</span></span>
<span data-ttu-id="1540c-108">O cmdlet **New-AzRmStorageShare** cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1540c-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="1540c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1540c-109">EXAMPLES</span></span>

### <span data-ttu-id="1540c-110">Exemplo 1: criar um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento, com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="1540c-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="1540c-111">Esse comando cria um compartilhamento de arquivos de armazenamento com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="1540c-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="1540c-112">Exemplo 2: criar um compartilhamento de arquivos de armazenamento com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1540c-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="1540c-113">Esse comando cria um compartilhamento de arquivos de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1540c-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="1540c-114">OS</span><span class="sxs-lookup"><span data-stu-id="1540c-114">PARAMETERS</span></span>

### <span data-ttu-id="1540c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1540c-115">-DefaultProfile</span></span>
<span data-ttu-id="1540c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1540c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1540c-117">-Metadados</span><span class="sxs-lookup"><span data-stu-id="1540c-117">-Metadata</span></span>
<span data-ttu-id="1540c-118">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="1540c-118">Share Metadata</span></span>

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

### <span data-ttu-id="1540c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1540c-119">-Name</span></span>
<span data-ttu-id="1540c-120">Nome do compartilhamento de arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="1540c-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1540c-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="1540c-121">-QuotaGiB</span></span>
<span data-ttu-id="1540c-122">Compartilhe a cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="1540c-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1540c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1540c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1540c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1540c-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1540c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1540c-125">-StorageAccount</span></span>
<span data-ttu-id="1540c-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1540c-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1540c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1540c-127">-StorageAccountName</span></span>
<span data-ttu-id="1540c-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1540c-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1540c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1540c-129">-Confirm</span></span>
<span data-ttu-id="1540c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1540c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1540c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1540c-131">-WhatIf</span></span>
<span data-ttu-id="1540c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1540c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1540c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1540c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1540c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1540c-134">CommonParameters</span></span>
<span data-ttu-id="1540c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1540c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1540c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1540c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1540c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1540c-137">INPUTS</span></span>

### <span data-ttu-id="1540c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1540c-138">System.String</span></span>

### <span data-ttu-id="1540c-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1540c-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1540c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1540c-140">OUTPUTS</span></span>

### <span data-ttu-id="1540c-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="1540c-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="1540c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1540c-142">NOTES</span></span>

## <span data-ttu-id="1540c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1540c-143">RELATED LINKS</span></span>
