---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 7b66dff3f59e3ad186bfc559343aebf484ff2bc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399611"
---
# <span data-ttu-id="de3cf-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="de3cf-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="de3cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="de3cf-103">Exclui o aplicativo azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de3cf-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="de3cf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de3cf-104">SYNTAX</span></span>

### <span data-ttu-id="de3cf-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de3cf-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3cf-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de3cf-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3cf-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de3cf-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3cf-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de3cf-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3cf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="de3cf-109">DESCRIPTION</span></span>
<span data-ttu-id="de3cf-110">Exclui o aplicativo do azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de3cf-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="de3cf-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de3cf-111">EXAMPLES</span></span>

### <span data-ttu-id="de3cf-112">Exemplo 1 - Remover aplicativo por id de objeto</span><span class="sxs-lookup"><span data-stu-id="de3cf-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="de3cf-113">Remove o aplicativo com a ID do objeto 'b4cd1619-80b3-4cfb-9f8f-9f233425738' do locatário.</span><span class="sxs-lookup"><span data-stu-id="de3cf-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="de3cf-114">Exemplo 2 - Remover aplicativo por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="de3cf-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="de3cf-115">Remove o aplicativo com a ID do aplicativo 'f9c5ea4f-28f0-401a-a491-491a037fa346' do locatário.</span><span class="sxs-lookup"><span data-stu-id="de3cf-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="de3cf-116">Exemplo 3 - Remover aplicativo por piping</span><span class="sxs-lookup"><span data-stu-id="de3cf-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="de3cf-117">Obtém o aplicativo com a ID do objeto 'b4cd1619-80b3-4cfb-9f8f-9f233425738' e os canos que vão para o cmdlet Remove-AzADApplication para remover o aplicativo do locatário.</span><span class="sxs-lookup"><span data-stu-id="de3cf-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="de3cf-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3cf-118">PARAMETERS</span></span>

### <span data-ttu-id="de3cf-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="de3cf-119">-ApplicationId</span></span>
<span data-ttu-id="de3cf-120">A ID do aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="de3cf-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="de3cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3cf-121">-DefaultProfile</span></span>
<span data-ttu-id="de3cf-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="de3cf-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de3cf-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de3cf-123">-DisplayName</span></span>
<span data-ttu-id="de3cf-124">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de3cf-124">The display name of the application.</span></span>

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

### <span data-ttu-id="de3cf-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="de3cf-125">-Force</span></span>
<span data-ttu-id="de3cf-126">Alternar para excluir um aplicativo sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="de3cf-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="de3cf-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de3cf-127">-InputObject</span></span>
<span data-ttu-id="de3cf-128">O objeto que representa o aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="de3cf-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="de3cf-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="de3cf-129">-ObjectId</span></span>
<span data-ttu-id="de3cf-130">A ID do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="de3cf-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="de3cf-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de3cf-131">-PassThru</span></span>
<span data-ttu-id="de3cf-132">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="de3cf-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="de3cf-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="de3cf-133">-Confirm</span></span>
<span data-ttu-id="de3cf-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3cf-135">-WhatIf</span></span>
<span data-ttu-id="de3cf-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="de3cf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de3cf-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de3cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3cf-138">CommonParameters</span></span>
<span data-ttu-id="de3cf-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3cf-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3cf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3cf-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="de3cf-141">INPUTS</span></span>

### <span data-ttu-id="de3cf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="de3cf-142">System.String</span></span>

### <span data-ttu-id="de3cf-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="de3cf-143">System.Guid</span></span>

### <span data-ttu-id="de3cf-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="de3cf-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="de3cf-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="de3cf-145">OUTPUTS</span></span>

### <span data-ttu-id="de3cf-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de3cf-146">System.Boolean</span></span>

## <span data-ttu-id="de3cf-147">Notas</span><span class="sxs-lookup"><span data-stu-id="de3cf-147">NOTES</span></span>
<span data-ttu-id="de3cf-148">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="de3cf-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="de3cf-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de3cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="de3cf-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="de3cf-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="de3cf-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="de3cf-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="de3cf-152">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="de3cf-152">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

