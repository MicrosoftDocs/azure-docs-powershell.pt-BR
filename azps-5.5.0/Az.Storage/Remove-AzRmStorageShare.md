---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114413"
---
# <span data-ttu-id="2db6f-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2db6f-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="2db6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2db6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2db6f-103">Remove um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2db6f-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="2db6f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2db6f-104">SYNTAX</span></span>

### <span data-ttu-id="2db6f-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2db6f-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db6f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2db6f-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db6f-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="2db6f-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db6f-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="2db6f-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db6f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2db6f-109">DESCRIPTION</span></span>
<span data-ttu-id="2db6f-110">O **cmdlet New-AzRmStorageShare** remove um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2db6f-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="2db6f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2db6f-111">EXAMPLES</span></span>

### <span data-ttu-id="2db6f-112">Exemplo 1: Remover um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="2db6f-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="2db6f-113">Esse comando remove um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2db6f-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="2db6f-114">Exemplo 2: Remover um compartilhamento de arquivo de armazenamento com objeto de conta de armazenamento e compartilhar nome</span><span class="sxs-lookup"><span data-stu-id="2db6f-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="2db6f-115">Esse comando remove um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2db6f-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="2db6f-116">Exemplo 3: Remover todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="2db6f-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="2db6f-117">Esse comando remove todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="2db6f-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="2db6f-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2db6f-118">PARAMETERS</span></span>

### <span data-ttu-id="2db6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db6f-119">-DefaultProfile</span></span>
<span data-ttu-id="2db6f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2db6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db6f-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2db6f-121">-Force</span></span>
<span data-ttu-id="2db6f-122">Forçar a remoção do Compartilhamento e todo o conteúdo nele</span><span class="sxs-lookup"><span data-stu-id="2db6f-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="2db6f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db6f-123">-InputObject</span></span>
<span data-ttu-id="2db6f-124">Objeto Compartilhamento de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2db6f-124">Storage Share object</span></span>

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

### <span data-ttu-id="2db6f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2db6f-125">-Name</span></span>
<span data-ttu-id="2db6f-126">Compartilhar Nome</span><span class="sxs-lookup"><span data-stu-id="2db6f-126">Share Name</span></span>

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

### <span data-ttu-id="2db6f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2db6f-127">-PassThru</span></span>
<span data-ttu-id="2db6f-128">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="2db6f-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2db6f-129">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2db6f-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2db6f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db6f-130">-ResourceGroupName</span></span>
<span data-ttu-id="2db6f-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2db6f-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2db6f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2db6f-132">-ResourceId</span></span>
<span data-ttu-id="2db6f-133">Inserir uma ID de Recurso de Compartilhamento de Arquivo.</span><span class="sxs-lookup"><span data-stu-id="2db6f-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="2db6f-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db6f-134">-StorageAccount</span></span>
<span data-ttu-id="2db6f-135">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2db6f-135">Storage account object</span></span>

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

### <span data-ttu-id="2db6f-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2db6f-136">-StorageAccountName</span></span>
<span data-ttu-id="2db6f-137">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2db6f-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="2db6f-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2db6f-138">-Confirm</span></span>
<span data-ttu-id="2db6f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db6f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db6f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db6f-140">-WhatIf</span></span>
<span data-ttu-id="2db6f-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2db6f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db6f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2db6f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db6f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db6f-143">CommonParameters</span></span>
<span data-ttu-id="2db6f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db6f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db6f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db6f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db6f-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="2db6f-146">INPUTS</span></span>

### <span data-ttu-id="2db6f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2db6f-147">System.String</span></span>

### <span data-ttu-id="2db6f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db6f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2db6f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="2db6f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="2db6f-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="2db6f-150">OUTPUTS</span></span>

### <span data-ttu-id="2db6f-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2db6f-151">System.Boolean</span></span>

## <span data-ttu-id="2db6f-152">Notas</span><span class="sxs-lookup"><span data-stu-id="2db6f-152">NOTES</span></span>

## <span data-ttu-id="2db6f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2db6f-153">RELATED LINKS</span></span>
