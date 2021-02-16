---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113679"
---
# <span data-ttu-id="70986-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="70986-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="70986-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70986-102">SYNOPSIS</span></span>
<span data-ttu-id="70986-103">Adiciona marcas de entalhe legal a um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="70986-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="70986-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70986-104">SYNTAX</span></span>

### <span data-ttu-id="70986-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70986-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70986-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="70986-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70986-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="70986-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70986-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70986-108">DESCRIPTION</span></span>
<span data-ttu-id="70986-109">O **cmdlet Add-AzRmStorageContainerLegalHold** adiciona marcas de bloqueio legal a um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="70986-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="70986-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70986-110">EXAMPLES</span></span>

### <span data-ttu-id="70986-111">Exemplo 1: Adicionar marcas de responsabilidade legal a um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="70986-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="70986-112">Esse comando adiciona marcas de responsabilidade legal a um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70986-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="70986-113">Exemplo 2: Adicionar marcas de responsabilidade legal a um contêiner de blob armazenamento com o objeto da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="70986-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="70986-114">Esse comando adiciona marcas de responsabilidade legal a um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70986-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="70986-115">Exemplo 3: Adicionar marcas de responsabilidade legal a todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="70986-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="70986-116">Esse comando adiciona marcas de responsabilidade legal a todos os contêineres de blob de armazenamento em uma conta de Armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="70986-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="70986-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70986-117">PARAMETERS</span></span>

### <span data-ttu-id="70986-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="70986-118">-Container</span></span>
<span data-ttu-id="70986-119">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70986-119">Storage container object</span></span>

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

### <span data-ttu-id="70986-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70986-120">-DefaultProfile</span></span>
<span data-ttu-id="70986-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="70986-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70986-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="70986-122">-Name</span></span>
<span data-ttu-id="70986-123">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="70986-123">Container Name</span></span>

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

### <span data-ttu-id="70986-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70986-124">-ResourceGroupName</span></span>
<span data-ttu-id="70986-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70986-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="70986-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="70986-126">-StorageAccount</span></span>
<span data-ttu-id="70986-127">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70986-127">Storage account object</span></span>

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

### <span data-ttu-id="70986-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70986-128">-StorageAccountName</span></span>
<span data-ttu-id="70986-129">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70986-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="70986-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="70986-130">-Tag</span></span>
<span data-ttu-id="70986-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="70986-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="70986-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="70986-132">-Confirm</span></span>
<span data-ttu-id="70986-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70986-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70986-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70986-134">-WhatIf</span></span>
<span data-ttu-id="70986-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="70986-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70986-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70986-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70986-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70986-137">CommonParameters</span></span>
<span data-ttu-id="70986-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70986-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70986-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70986-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70986-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="70986-140">INPUTS</span></span>

### <span data-ttu-id="70986-141">System.String</span><span class="sxs-lookup"><span data-stu-id="70986-141">System.String</span></span>

### <span data-ttu-id="70986-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70986-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="70986-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="70986-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="70986-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="70986-144">OUTPUTS</span></span>

### <span data-ttu-id="70986-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="70986-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="70986-146">Notas</span><span class="sxs-lookup"><span data-stu-id="70986-146">NOTES</span></span>

## <span data-ttu-id="70986-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70986-147">RELATED LINKS</span></span>
