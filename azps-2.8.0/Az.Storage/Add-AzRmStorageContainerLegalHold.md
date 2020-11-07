---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 13fc089db38bb9aa525285c61b1a2d4fecd934b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774013"
---
# <span data-ttu-id="8c377-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="8c377-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="8c377-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c377-102">SYNOPSIS</span></span>
<span data-ttu-id="8c377-103">Adiciona marcas de retenção legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8c377-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="8c377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c377-104">SYNTAX</span></span>

### <span data-ttu-id="8c377-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c377-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c377-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="8c377-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c377-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c377-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c377-108">DESCRIPTION</span></span>
<span data-ttu-id="8c377-109">O cmdlet **Add-AzRmStorageContainerLegalHold** adiciona marcas de retenção legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8c377-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="8c377-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c377-110">EXAMPLES</span></span>

### <span data-ttu-id="8c377-111">Exemplo 1: adicionar marcas de retenção legal a um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="8c377-112">Esse comando adiciona marcas de retenção legal a um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8c377-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8c377-113">Exemplo 2: adicionar marcas de retenção legal a um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="8c377-114">Esse comando adiciona marcas de retenção legal a um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8c377-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8c377-115">Exemplo 3: adicionar marcas de retenção legal a todos os contêineres de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="8c377-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="8c377-116">Esse comando adiciona marcas de retenção legal a todos os contêineres de armazenamento de BLOB em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="8c377-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8c377-117">OS</span><span class="sxs-lookup"><span data-stu-id="8c377-117">PARAMETERS</span></span>

### <span data-ttu-id="8c377-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-118">-Container</span></span>
<span data-ttu-id="8c377-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8c377-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c377-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c377-120">-DefaultProfile</span></span>
<span data-ttu-id="8c377-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c377-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c377-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c377-122">-Name</span></span>
<span data-ttu-id="8c377-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c377-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c377-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c377-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c377-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c377-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c377-126">-StorageAccount</span></span>
<span data-ttu-id="8c377-127">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8c377-127">Storage account object</span></span>

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

### <span data-ttu-id="8c377-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c377-128">-StorageAccountName</span></span>
<span data-ttu-id="8c377-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8c377-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="8c377-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="8c377-130">-Tag</span></span>
<span data-ttu-id="8c377-131">Marcas LegalHold do contêiner</span><span class="sxs-lookup"><span data-stu-id="8c377-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c377-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c377-132">-Confirm</span></span>
<span data-ttu-id="8c377-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c377-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c377-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c377-134">-WhatIf</span></span>
<span data-ttu-id="8c377-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c377-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c377-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c377-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c377-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c377-137">CommonParameters</span></span>
<span data-ttu-id="8c377-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c377-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c377-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c377-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c377-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c377-140">INPUTS</span></span>

### <span data-ttu-id="8c377-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8c377-141">System.String</span></span>

### <span data-ttu-id="8c377-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c377-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8c377-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8c377-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8c377-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c377-144">OUTPUTS</span></span>

### <span data-ttu-id="8c377-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="8c377-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="8c377-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c377-146">NOTES</span></span>

## <span data-ttu-id="8c377-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c377-147">RELATED LINKS</span></span>