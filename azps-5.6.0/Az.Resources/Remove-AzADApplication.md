---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: d4415b2f97cb92c8694c0ca56a3b47d751a065f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889757"
---
# <span data-ttu-id="9def8-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9def8-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="9def8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9def8-102">SYNOPSIS</span></span>
<span data-ttu-id="9def8-103">Exclui o aplicativo do azure active directory.</span><span class="sxs-lookup"><span data-stu-id="9def8-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="9def8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9def8-104">SYNTAX</span></span>

### <span data-ttu-id="9def8-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9def8-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9def8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9def8-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9def8-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9def8-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9def8-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9def8-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9def8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9def8-109">DESCRIPTION</span></span>
<span data-ttu-id="9def8-110">Exclui o aplicativo do azure active directory.</span><span class="sxs-lookup"><span data-stu-id="9def8-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="9def8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9def8-111">EXAMPLES</span></span>

### <span data-ttu-id="9def8-112">Exemplo 1: Remover aplicativo por id de objeto</span><span class="sxs-lookup"><span data-stu-id="9def8-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="9def8-113">Remove o aplicativo com a id do objeto 'b4cd1619-80b3-4cfb-9f8f-9f233425738' do locatário.</span><span class="sxs-lookup"><span data-stu-id="9def8-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="9def8-114">Exemplo 2: Remover aplicativo por id de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9def8-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="9def8-115">Remove o aplicativo com a id do aplicativo 'f9c5ea4f-28f0-401a-a491-491a037fa346' do locatário.</span><span class="sxs-lookup"><span data-stu-id="9def8-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="9def8-116">Exemplo 3: Remover aplicativo por canalização</span><span class="sxs-lookup"><span data-stu-id="9def8-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="9def8-117">Obtém o aplicativo com a id do objeto 'b4cd1619-80b3-4cfb-9f8f-9f233425738' e canalização para o cmdlet Remove-AzADApplication para remover o aplicativo do locatário.</span><span class="sxs-lookup"><span data-stu-id="9def8-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="9def8-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9def8-118">PARAMETERS</span></span>

### <span data-ttu-id="9def8-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9def8-119">-ApplicationId</span></span>
<span data-ttu-id="9def8-120">A id do aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9def8-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9def8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9def8-121">-DefaultProfile</span></span>
<span data-ttu-id="9def8-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9def8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9def8-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9def8-123">-DisplayName</span></span>
<span data-ttu-id="9def8-124">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9def8-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9def8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9def8-125">-Force</span></span>
<span data-ttu-id="9def8-126">Alternar para excluir um aplicativo sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="9def8-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="9def8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9def8-127">-InputObject</span></span>
<span data-ttu-id="9def8-128">O objeto que representa o aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9def8-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9def8-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9def8-129">-ObjectId</span></span>
<span data-ttu-id="9def8-130">A id do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9def8-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9def8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9def8-131">-PassThru</span></span>
<span data-ttu-id="9def8-132">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9def8-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9def8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9def8-133">-Confirm</span></span>
<span data-ttu-id="9def8-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9def8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9def8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9def8-135">-WhatIf</span></span>
<span data-ttu-id="9def8-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9def8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9def8-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9def8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9def8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9def8-138">CommonParameters</span></span>
<span data-ttu-id="9def8-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9def8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9def8-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9def8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9def8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9def8-141">INPUTS</span></span>

### <span data-ttu-id="9def8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9def8-142">System.String</span></span>

### <span data-ttu-id="9def8-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9def8-143">System.Guid</span></span>

### <span data-ttu-id="9def8-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9def8-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="9def8-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9def8-145">OUTPUTS</span></span>

### <span data-ttu-id="9def8-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9def8-146">System.Boolean</span></span>

## <span data-ttu-id="9def8-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="9def8-147">NOTES</span></span>
<span data-ttu-id="9def8-148">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="9def8-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9def8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9def8-149">RELATED LINKS</span></span>

[<span data-ttu-id="9def8-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9def8-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="9def8-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9def8-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="9def8-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9def8-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="9def8-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9def8-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

