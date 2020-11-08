---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116554"
---
# <span data-ttu-id="e2283-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e2283-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="e2283-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2283-102">SYNOPSIS</span></span>
<span data-ttu-id="e2283-103">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e2283-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="e2283-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2283-104">SYNTAX</span></span>

### <span data-ttu-id="e2283-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2283-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2283-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2283-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2283-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2283-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2283-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2283-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2283-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2283-109">DESCRIPTION</span></span>
<span data-ttu-id="e2283-110">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e2283-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="e2283-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2283-111">EXAMPLES</span></span>

### <span data-ttu-id="e2283-112">Exemplo 1: remover aplicativo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="e2283-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="e2283-113">Remove o aplicativo com a ID de objeto "b4cd1619-80b3-4cfb-9f8f-9f2333425738" do locatário.</span><span class="sxs-lookup"><span data-stu-id="e2283-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="e2283-114">Exemplo 2: remover aplicativo por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e2283-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="e2283-115">Remove o aplicativo com a ID de aplicativo ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' do locatário.</span><span class="sxs-lookup"><span data-stu-id="e2283-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="e2283-116">Exemplo 3: remover o aplicativo por tubulação</span><span class="sxs-lookup"><span data-stu-id="e2283-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="e2283-117">Obtém o aplicativo com a ID de objeto ' b4cd1619-80b3-4cfb-9f8f-9f2333425738 ' e canaliza-se para o cmdlet Remove-AzADApplication para remover o aplicativo do locatário.</span><span class="sxs-lookup"><span data-stu-id="e2283-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="e2283-118">OS</span><span class="sxs-lookup"><span data-stu-id="e2283-118">PARAMETERS</span></span>

### <span data-ttu-id="e2283-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e2283-119">-ApplicationId</span></span>
<span data-ttu-id="e2283-120">A ID do aplicativo a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e2283-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="e2283-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2283-121">-DefaultProfile</span></span>
<span data-ttu-id="e2283-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e2283-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2283-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e2283-123">-DisplayName</span></span>
<span data-ttu-id="e2283-124">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2283-124">The display name of the application.</span></span>

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

### <span data-ttu-id="e2283-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e2283-125">-Force</span></span>
<span data-ttu-id="e2283-126">Alternar para excluir um aplicativo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="e2283-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="e2283-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2283-127">-InputObject</span></span>
<span data-ttu-id="e2283-128">O objeto que representa o aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e2283-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="e2283-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e2283-129">-ObjectId</span></span>
<span data-ttu-id="e2283-130">A ID do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e2283-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="e2283-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2283-131">-PassThru</span></span>
<span data-ttu-id="e2283-132">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e2283-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e2283-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2283-133">-Confirm</span></span>
<span data-ttu-id="e2283-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2283-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2283-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2283-135">-WhatIf</span></span>
<span data-ttu-id="e2283-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2283-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2283-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2283-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2283-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2283-138">CommonParameters</span></span>
<span data-ttu-id="e2283-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2283-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2283-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2283-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2283-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2283-141">INPUTS</span></span>

### <span data-ttu-id="e2283-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e2283-142">System.String</span></span>

### <span data-ttu-id="e2283-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e2283-143">System.Guid</span></span>

### <span data-ttu-id="e2283-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e2283-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e2283-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2283-145">OUTPUTS</span></span>

### <span data-ttu-id="e2283-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2283-146">System.Boolean</span></span>

## <span data-ttu-id="e2283-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2283-147">NOTES</span></span>
<span data-ttu-id="e2283-148">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="e2283-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e2283-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2283-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2283-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e2283-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="e2283-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e2283-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e2283-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e2283-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="e2283-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e2283-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

