---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114419"
---
# <span data-ttu-id="eca70-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eca70-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="eca70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eca70-102">SYNOPSIS</span></span>
<span data-ttu-id="eca70-103">Remove um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="eca70-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="eca70-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eca70-104">SYNTAX</span></span>

### <span data-ttu-id="eca70-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eca70-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca70-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="eca70-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca70-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="eca70-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca70-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="eca70-108">DESCRIPTION</span></span>
<span data-ttu-id="eca70-109">O cmdlet **Remove-AzRmStorageContainer** remove um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="eca70-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="eca70-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eca70-110">EXAMPLES</span></span>

### <span data-ttu-id="eca70-111">Exemplo 1: Remover um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="eca70-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="eca70-112">Esse comando remove um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="eca70-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="eca70-113">Exemplo 2: Remover um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="eca70-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="eca70-114">Esse comando remove um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="eca70-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="eca70-115">Exemplo 3: Remover todos os contêineres de blob armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="eca70-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="eca70-116">Esse comando remove todos os contêineres de blob armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="eca70-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="eca70-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eca70-117">PARAMETERS</span></span>

### <span data-ttu-id="eca70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca70-118">-DefaultProfile</span></span>
<span data-ttu-id="eca70-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eca70-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eca70-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="eca70-120">-Force</span></span>
<span data-ttu-id="eca70-121">Forçar a remoção do contêiner e todo o conteúdo nele</span><span class="sxs-lookup"><span data-stu-id="eca70-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca70-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca70-122">-InputObject</span></span>
<span data-ttu-id="eca70-123">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eca70-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca70-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eca70-124">-Name</span></span>
<span data-ttu-id="eca70-125">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="eca70-125">Container Name</span></span>

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

### <span data-ttu-id="eca70-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eca70-126">-PassThru</span></span>
<span data-ttu-id="eca70-127">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="eca70-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eca70-128">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eca70-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eca70-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca70-129">-ResourceGroupName</span></span>
<span data-ttu-id="eca70-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eca70-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="eca70-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="eca70-131">-StorageAccount</span></span>
<span data-ttu-id="eca70-132">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eca70-132">Storage account object</span></span>

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

### <span data-ttu-id="eca70-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eca70-133">-StorageAccountName</span></span>
<span data-ttu-id="eca70-134">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eca70-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="eca70-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eca70-135">-Confirm</span></span>
<span data-ttu-id="eca70-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca70-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca70-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca70-137">-WhatIf</span></span>
<span data-ttu-id="eca70-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eca70-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eca70-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eca70-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca70-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca70-140">CommonParameters</span></span>
<span data-ttu-id="eca70-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca70-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca70-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca70-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca70-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="eca70-143">INPUTS</span></span>

### <span data-ttu-id="eca70-144">System.String</span><span class="sxs-lookup"><span data-stu-id="eca70-144">System.String</span></span>

### <span data-ttu-id="eca70-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eca70-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="eca70-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="eca70-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="eca70-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="eca70-147">OUTPUTS</span></span>

### <span data-ttu-id="eca70-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eca70-148">System.Boolean</span></span>

## <span data-ttu-id="eca70-149">Notas</span><span class="sxs-lookup"><span data-stu-id="eca70-149">NOTES</span></span>

## <span data-ttu-id="eca70-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eca70-150">RELATED LINKS</span></span>
