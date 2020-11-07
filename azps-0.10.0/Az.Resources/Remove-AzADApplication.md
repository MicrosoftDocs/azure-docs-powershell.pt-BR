---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 00c9d6e5a5a729ca5a5119b812873078acb38326
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776368"
---
# <span data-ttu-id="dddfc-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dddfc-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="dddfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dddfc-102">SYNOPSIS</span></span>
<span data-ttu-id="dddfc-103">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dddfc-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="dddfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dddfc-104">SYNTAX</span></span>

### <span data-ttu-id="dddfc-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dddfc-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dddfc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dddfc-109">DESCRIPTION</span></span>
<span data-ttu-id="dddfc-110">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dddfc-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="dddfc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dddfc-111">EXAMPLES</span></span>

### <span data-ttu-id="dddfc-112">Exemplo 1-remover aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="dddfc-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="dddfc-113">Remove o aplicativo com a ID de objeto "b4cd1619-80b3-4cfb-9f8f-9f2333425738" do locatário.</span><span class="sxs-lookup"><span data-stu-id="dddfc-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="dddfc-114">Exemplo 2-remover aplicativo por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="dddfc-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="dddfc-115">Remove o aplicativo com a ID de aplicativo ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' do locatário.</span><span class="sxs-lookup"><span data-stu-id="dddfc-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="dddfc-116">Exemplo 3-remover o aplicativo por meio do encanamento</span><span class="sxs-lookup"><span data-stu-id="dddfc-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="dddfc-117">Obtém o aplicativo com a ID de objeto ' b4cd1619-80b3-4cfb-9f8f-9f2333425738 ' e canaliza-se para o cmdlet Remove-AzADApplication para remover o aplicativo do locatário.</span><span class="sxs-lookup"><span data-stu-id="dddfc-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="dddfc-118">OS</span><span class="sxs-lookup"><span data-stu-id="dddfc-118">PARAMETERS</span></span>

### <span data-ttu-id="dddfc-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dddfc-119">-ApplicationId</span></span>
<span data-ttu-id="dddfc-120">A ID do aplicativo a ser removida.</span><span class="sxs-lookup"><span data-stu-id="dddfc-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="dddfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddfc-121">-DefaultProfile</span></span>
<span data-ttu-id="dddfc-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dddfc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddfc-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dddfc-123">-DisplayName</span></span>
<span data-ttu-id="dddfc-124">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dddfc-124">The display name of the application.</span></span>

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

### <span data-ttu-id="dddfc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dddfc-125">-Force</span></span>
<span data-ttu-id="dddfc-126">Alternar para excluir um aplicativo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="dddfc-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="dddfc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-127">-InputObject</span></span>
<span data-ttu-id="dddfc-128">O objeto que representa o aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="dddfc-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dddfc-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dddfc-129">-ObjectId</span></span>
<span data-ttu-id="dddfc-130">A ID do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="dddfc-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddfc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dddfc-131">-PassThru</span></span>
<span data-ttu-id="dddfc-132">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dddfc-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dddfc-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dddfc-133">-Confirm</span></span>
<span data-ttu-id="dddfc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dddfc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dddfc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dddfc-135">-WhatIf</span></span>
<span data-ttu-id="dddfc-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dddfc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dddfc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dddfc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dddfc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddfc-138">CommonParameters</span></span>
<span data-ttu-id="dddfc-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dddfc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddfc-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddfc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddfc-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dddfc-141">INPUTS</span></span>

### <span data-ttu-id="dddfc-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dddfc-142">System.Guid</span></span>

### <span data-ttu-id="dddfc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-143">System.String</span></span>

### <span data-ttu-id="dddfc-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dddfc-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="dddfc-145">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dddfc-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dddfc-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dddfc-146">OUTPUTS</span></span>

### <span data-ttu-id="dddfc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dddfc-147">System.Boolean</span></span>

## <span data-ttu-id="dddfc-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dddfc-148">NOTES</span></span>
<span data-ttu-id="dddfc-149">Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="dddfc-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dddfc-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dddfc-150">RELATED LINKS</span></span>

[<span data-ttu-id="dddfc-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dddfc-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="dddfc-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dddfc-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="dddfc-153">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dddfc-153">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="dddfc-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dddfc-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

