---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: ca2db2ece85860c9aeae8e45909cdb5135beaae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891275"
---
# <span data-ttu-id="0799c-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0799c-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="0799c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0799c-102">SYNOPSIS</span></span>
<span data-ttu-id="0799c-103">Remove um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0799c-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="0799c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0799c-104">SYNTAX</span></span>

### <span data-ttu-id="0799c-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0799c-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0799c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0799c-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0799c-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="0799c-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0799c-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="0799c-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0799c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0799c-109">DESCRIPTION</span></span>
<span data-ttu-id="0799c-110">O cmdlet **New-AzRmStorageShare** remove um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0799c-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="0799c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0799c-111">EXAMPLES</span></span>

### <span data-ttu-id="0799c-112">Exemplo 1: Remover um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0799c-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="0799c-113">Este comando remove um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0799c-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="0799c-114">Exemplo 2: Remover um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0799c-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="0799c-115">Este comando remove um compartilhamento de arquivo de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0799c-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="0799c-116">Exemplo 3: Remover todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="0799c-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="0799c-117">Este comando remove todos os compartilhamentos de arquivo de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="0799c-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="0799c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0799c-118">PARAMETERS</span></span>

### <span data-ttu-id="0799c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0799c-119">-DefaultProfile</span></span>
<span data-ttu-id="0799c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0799c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0799c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0799c-121">-Force</span></span>
<span data-ttu-id="0799c-122">Forçar a remover o Compartilhamento e todo o conteúdo nele</span><span class="sxs-lookup"><span data-stu-id="0799c-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="0799c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0799c-123">-InputObject</span></span>
<span data-ttu-id="0799c-124">Objeto Storage Share</span><span class="sxs-lookup"><span data-stu-id="0799c-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0799c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0799c-125">-Name</span></span>
<span data-ttu-id="0799c-126">Nome do Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0799c-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0799c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0799c-127">-PassThru</span></span>
<span data-ttu-id="0799c-128">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="0799c-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0799c-129">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0799c-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0799c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0799c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0799c-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0799c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="0799c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0799c-132">-ResourceId</span></span>
<span data-ttu-id="0799c-133">Entrada de uma ID de Recurso de Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="0799c-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="0799c-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0799c-134">-StorageAccount</span></span>
<span data-ttu-id="0799c-135">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0799c-135">Storage account object</span></span>

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

### <span data-ttu-id="0799c-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0799c-136">-StorageAccountName</span></span>
<span data-ttu-id="0799c-137">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0799c-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="0799c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0799c-138">-Confirm</span></span>
<span data-ttu-id="0799c-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0799c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0799c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0799c-140">-WhatIf</span></span>
<span data-ttu-id="0799c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0799c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0799c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0799c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0799c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0799c-143">CommonParameters</span></span>
<span data-ttu-id="0799c-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0799c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0799c-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0799c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0799c-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0799c-146">INPUTS</span></span>

### <span data-ttu-id="0799c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0799c-147">System.String</span></span>

### <span data-ttu-id="0799c-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0799c-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0799c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="0799c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0799c-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0799c-150">OUTPUTS</span></span>

### <span data-ttu-id="0799c-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0799c-151">System.Boolean</span></span>

## <span data-ttu-id="0799c-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="0799c-152">NOTES</span></span>

## <span data-ttu-id="0799c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0799c-153">RELATED LINKS</span></span>
