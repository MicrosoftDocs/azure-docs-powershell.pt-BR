---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260943"
---
# <span data-ttu-id="b3e3e-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b3e3e-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="b3e3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e3e-103">Remove um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="b3e3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3e3e-104">SYNTAX</span></span>

### <span data-ttu-id="b3e3e-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3e3e-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e3e-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="b3e3e-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e3e-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e3e-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e3e-108">Shareobject</span><span class="sxs-lookup"><span data-stu-id="b3e3e-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e3e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3e3e-109">DESCRIPTION</span></span>
<span data-ttu-id="b3e3e-110">O cmdlet **New-AzRmStorageShare** remove um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="b3e3e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3e3e-111">EXAMPLES</span></span>

### <span data-ttu-id="b3e3e-112">Exemplo 1: remover um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b3e3e-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="b3e3e-113">Esse comando Remove um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="b3e3e-114">Exemplo 2: remover um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b3e3e-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="b3e3e-115">Esse comando Remove um compartilhamento de arquivos de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="b3e3e-116">Exemplo 3: remover todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="b3e3e-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="b3e3e-117">Esse comando Remove todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b3e3e-118">OS</span><span class="sxs-lookup"><span data-stu-id="b3e3e-118">PARAMETERS</span></span>

### <span data-ttu-id="b3e3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e3e-119">-DefaultProfile</span></span>
<span data-ttu-id="b3e3e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e3e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b3e3e-121">-Force</span></span>
<span data-ttu-id="b3e3e-122">Forçar a remoção do compartilhamento e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="b3e3e-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="b3e3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e3e-123">-InputObject</span></span>
<span data-ttu-id="b3e3e-124">Objeto de compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b3e3e-124">Storage Share object</span></span>

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

### <span data-ttu-id="b3e3e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3e3e-125">-Name</span></span>
<span data-ttu-id="b3e3e-126">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b3e3e-126">Share Name</span></span>

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

### <span data-ttu-id="b3e3e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3e3e-127">-PassThru</span></span>
<span data-ttu-id="b3e3e-128">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b3e3e-129">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b3e3e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e3e-130">-ResourceGroupName</span></span>
<span data-ttu-id="b3e3e-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3e3e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e3e-132">-ResourceId</span></span>
<span data-ttu-id="b3e3e-133">Insira uma ID de recurso de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="b3e3e-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3e3e-134">-StorageAccount</span></span>
<span data-ttu-id="b3e3e-135">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b3e3e-135">Storage account object</span></span>

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

### <span data-ttu-id="b3e3e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b3e3e-136">-StorageAccountName</span></span>
<span data-ttu-id="b3e3e-137">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="b3e3e-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3e3e-138">-Confirm</span></span>
<span data-ttu-id="b3e3e-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e3e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e3e-140">-WhatIf</span></span>
<span data-ttu-id="b3e3e-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e3e-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e3e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e3e-143">CommonParameters</span></span>
<span data-ttu-id="b3e3e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e3e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e3e-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e3e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e3e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3e3e-146">INPUTS</span></span>

### <span data-ttu-id="b3e3e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e3e-147">System.String</span></span>

### <span data-ttu-id="b3e3e-148">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3e3e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b3e3e-149">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="b3e3e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="b3e3e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3e3e-150">OUTPUTS</span></span>

### <span data-ttu-id="b3e3e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3e3e-151">System.Boolean</span></span>

## <span data-ttu-id="b3e3e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3e3e-152">NOTES</span></span>

## <span data-ttu-id="b3e3e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3e3e-153">RELATED LINKS</span></span>
