---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 8b0608a350f73de4280380abf7fd213d48742022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888410"
---
# <span data-ttu-id="35c02-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="35c02-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="35c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35c02-102">SYNOPSIS</span></span>
<span data-ttu-id="35c02-103">Adiciona marcas de ressarção legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="35c02-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="35c02-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35c02-104">SYNTAX</span></span>

### <span data-ttu-id="35c02-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="35c02-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c02-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="35c02-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c02-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="35c02-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35c02-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35c02-108">DESCRIPTION</span></span>
<span data-ttu-id="35c02-109">O cmdlet **Add-AzRmStorageContainerLegalHold** adiciona marcas de bloqueio legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="35c02-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="35c02-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35c02-110">EXAMPLES</span></span>

### <span data-ttu-id="35c02-111">Exemplo 1: Adicionar marcas de responsabilidade legal a um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="35c02-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="35c02-112">Este comando adiciona marcas de responsabilidade legal a um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="35c02-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="35c02-113">Exemplo 2: Adicionar marcas de responsabilidade legal a um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="35c02-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="35c02-114">Este comando adiciona marcas de responsabilidade legal a um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="35c02-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="35c02-115">Exemplo 3: Adicionar marcas de responsabilidade legal a todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="35c02-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="35c02-116">Este comando adiciona marcas de responsabilidade legal a todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="35c02-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="35c02-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35c02-117">PARAMETERS</span></span>

### <span data-ttu-id="35c02-118">-Container</span><span class="sxs-lookup"><span data-stu-id="35c02-118">-Container</span></span>
<span data-ttu-id="35c02-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="35c02-119">Storage container object</span></span>

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

### <span data-ttu-id="35c02-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c02-120">-DefaultProfile</span></span>
<span data-ttu-id="35c02-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="35c02-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c02-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35c02-122">-Name</span></span>
<span data-ttu-id="35c02-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="35c02-123">Container Name</span></span>

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

### <span data-ttu-id="35c02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c02-124">-ResourceGroupName</span></span>
<span data-ttu-id="35c02-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="35c02-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="35c02-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="35c02-126">-StorageAccount</span></span>
<span data-ttu-id="35c02-127">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="35c02-127">Storage account object</span></span>

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

### <span data-ttu-id="35c02-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35c02-128">-StorageAccountName</span></span>
<span data-ttu-id="35c02-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="35c02-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="35c02-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="35c02-130">-Tag</span></span>
<span data-ttu-id="35c02-131">Marcas De Contêiner LegalHold</span><span class="sxs-lookup"><span data-stu-id="35c02-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="35c02-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35c02-132">-Confirm</span></span>
<span data-ttu-id="35c02-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35c02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c02-134">-WhatIf</span></span>
<span data-ttu-id="35c02-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35c02-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35c02-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35c02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c02-137">CommonParameters</span></span>
<span data-ttu-id="35c02-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c02-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c02-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c02-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35c02-140">INPUTS</span></span>

### <span data-ttu-id="35c02-141">System.String</span><span class="sxs-lookup"><span data-stu-id="35c02-141">System.String</span></span>

### <span data-ttu-id="35c02-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35c02-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="35c02-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="35c02-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="35c02-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35c02-144">OUTPUTS</span></span>

### <span data-ttu-id="35c02-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="35c02-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="35c02-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="35c02-146">NOTES</span></span>

## <span data-ttu-id="35c02-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35c02-147">RELATED LINKS</span></span>
