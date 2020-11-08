---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118462"
---
# <span data-ttu-id="14775-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14775-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="14775-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14775-102">SYNOPSIS</span></span>
<span data-ttu-id="14775-103">Cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14775-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="14775-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14775-104">SYNTAX</span></span>

### <span data-ttu-id="14775-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="14775-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14775-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="14775-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14775-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14775-107">DESCRIPTION</span></span>
<span data-ttu-id="14775-108">O cmdlet **New-AzRmStorageContainer** cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14775-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="14775-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14775-109">EXAMPLES</span></span>

### <span data-ttu-id="14775-110">Exemplo 1: criar um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner com metadados</span><span class="sxs-lookup"><span data-stu-id="14775-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="14775-111">Esse comando cria um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner, com metadados.</span><span class="sxs-lookup"><span data-stu-id="14775-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="14775-112">Exemplo 2: criar um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner com acesso público como blob</span><span class="sxs-lookup"><span data-stu-id="14775-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="14775-113">Esse comando cria um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner com acesso público como BLOB.</span><span class="sxs-lookup"><span data-stu-id="14775-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="14775-114">OS</span><span class="sxs-lookup"><span data-stu-id="14775-114">PARAMETERS</span></span>

### <span data-ttu-id="14775-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14775-115">-DefaultProfile</span></span>
<span data-ttu-id="14775-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14775-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14775-117">-Metadados</span><span class="sxs-lookup"><span data-stu-id="14775-117">-Metadata</span></span>
<span data-ttu-id="14775-118">Metadados do contêiner</span><span class="sxs-lookup"><span data-stu-id="14775-118">Container Metadata</span></span>

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

### <span data-ttu-id="14775-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="14775-119">-Name</span></span>
<span data-ttu-id="14775-120">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="14775-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14775-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="14775-121">-PublicAccess</span></span>
<span data-ttu-id="14775-122">PublicAccess de contêiner</span><span class="sxs-lookup"><span data-stu-id="14775-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14775-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14775-123">-ResourceGroupName</span></span>
<span data-ttu-id="14775-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14775-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="14775-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="14775-125">-StorageAccount</span></span>
<span data-ttu-id="14775-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14775-126">Storage account object</span></span>

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

### <span data-ttu-id="14775-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14775-127">-StorageAccountName</span></span>
<span data-ttu-id="14775-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14775-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="14775-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14775-129">-Confirm</span></span>
<span data-ttu-id="14775-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14775-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14775-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14775-131">-WhatIf</span></span>
<span data-ttu-id="14775-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14775-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14775-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14775-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14775-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14775-134">CommonParameters</span></span>
<span data-ttu-id="14775-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14775-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14775-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14775-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14775-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14775-137">INPUTS</span></span>

### <span data-ttu-id="14775-138">System. String</span><span class="sxs-lookup"><span data-stu-id="14775-138">System.String</span></span>

### <span data-ttu-id="14775-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14775-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="14775-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14775-140">OUTPUTS</span></span>

### <span data-ttu-id="14775-141">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="14775-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="14775-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14775-142">NOTES</span></span>

## <span data-ttu-id="14775-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14775-143">RELATED LINKS</span></span>
