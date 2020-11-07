---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774208"
---
# <span data-ttu-id="f1039-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1039-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="f1039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1039-102">SYNOPSIS</span></span>
<span data-ttu-id="f1039-103">Remove um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1039-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="f1039-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1039-104">SYNTAX</span></span>

### <span data-ttu-id="f1039-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1039-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1039-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="f1039-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1039-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f1039-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1039-108">Shareobject</span><span class="sxs-lookup"><span data-stu-id="f1039-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1039-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1039-109">DESCRIPTION</span></span>
<span data-ttu-id="f1039-110">O cmdlet **New-AzRmStorageShare** remove um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1039-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="f1039-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1039-111">EXAMPLES</span></span>

### <span data-ttu-id="f1039-112">Exemplo 1: remover um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f1039-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="f1039-113">Esse comando Remove um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f1039-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="f1039-114">Exemplo 2: remover um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f1039-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="f1039-115">Esse comando Remove um compartilhamento de arquivos de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f1039-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="f1039-116">Exemplo 3: remover todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="f1039-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="f1039-117">Esse comando Remove todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1039-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f1039-118">OS</span><span class="sxs-lookup"><span data-stu-id="f1039-118">PARAMETERS</span></span>

### <span data-ttu-id="f1039-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1039-119">-DefaultProfile</span></span>
<span data-ttu-id="f1039-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1039-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1039-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1039-121">-Force</span></span>
<span data-ttu-id="f1039-122">Forçar a remoção do compartilhamento e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="f1039-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="f1039-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1039-123">-InputObject</span></span>
<span data-ttu-id="f1039-124">Objeto de compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1039-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1039-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1039-125">-Name</span></span>
<span data-ttu-id="f1039-126">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f1039-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1039-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1039-127">-PassThru</span></span>
<span data-ttu-id="f1039-128">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="f1039-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f1039-129">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f1039-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f1039-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1039-130">-ResourceGroupName</span></span>
<span data-ttu-id="f1039-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1039-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1039-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1039-132">-ResourceId</span></span>
<span data-ttu-id="f1039-133">Insira uma ID de recurso de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1039-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f1039-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1039-134">-StorageAccount</span></span>
<span data-ttu-id="f1039-135">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1039-135">Storage account object</span></span>

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

### <span data-ttu-id="f1039-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1039-136">-StorageAccountName</span></span>
<span data-ttu-id="f1039-137">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1039-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="f1039-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1039-138">-Confirm</span></span>
<span data-ttu-id="f1039-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1039-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1039-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1039-140">-WhatIf</span></span>
<span data-ttu-id="f1039-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1039-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1039-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1039-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1039-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1039-143">CommonParameters</span></span>
<span data-ttu-id="f1039-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1039-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1039-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1039-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1039-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1039-146">INPUTS</span></span>

### <span data-ttu-id="f1039-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f1039-147">System.String</span></span>

### <span data-ttu-id="f1039-148">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1039-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f1039-149">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f1039-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f1039-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1039-150">OUTPUTS</span></span>

### <span data-ttu-id="f1039-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1039-151">System.Boolean</span></span>

## <span data-ttu-id="f1039-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1039-152">NOTES</span></span>

## <span data-ttu-id="f1039-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1039-153">RELATED LINKS</span></span>
