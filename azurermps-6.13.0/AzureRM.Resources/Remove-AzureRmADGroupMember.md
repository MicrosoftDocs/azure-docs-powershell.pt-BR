---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602452"
---
# <span data-ttu-id="2832c-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="2832c-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="2832c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2832c-102">SYNOPSIS</span></span>
<span data-ttu-id="2832c-103">Remove um usuário de um grupo do AD.</span><span class="sxs-lookup"><span data-stu-id="2832c-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2832c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2832c-104">SYNTAX</span></span>

### <span data-ttu-id="2832c-105">ExplicitParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2832c-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2832c-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2832c-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2832c-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="2832c-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2832c-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="2832c-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2832c-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2832c-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2832c-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2832c-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2832c-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2832c-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2832c-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2832c-112">DESCRIPTION</span></span>
<span data-ttu-id="2832c-113">Remove um usuário de um grupo do AD.</span><span class="sxs-lookup"><span data-stu-id="2832c-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="2832c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2832c-114">EXAMPLES</span></span>

### <span data-ttu-id="2832c-115">Exemplo 1-remover um usuário de um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="2832c-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="2832c-116">Remove o usuário com a ID de objeto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" do grupo com a ID de objeto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="2832c-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="2832c-117">Exemplo 2-remover um usuário de um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="2832c-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="2832c-118">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e a canaliza para o cmdlet Remove-AzureRmADGroupMember para remover o usuário desse grupo.</span><span class="sxs-lookup"><span data-stu-id="2832c-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="2832c-119">OS</span><span class="sxs-lookup"><span data-stu-id="2832c-119">PARAMETERS</span></span>

### <span data-ttu-id="2832c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2832c-120">-DefaultProfile</span></span>
<span data-ttu-id="2832c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2832c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2832c-122">-GroupDisplayName</span></span>
<span data-ttu-id="2832c-123">O nome de exibição do grupo do qual você deseja remover o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="2832c-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="2832c-124">-GroupObject</span></span>
<span data-ttu-id="2832c-125">A representação de objeto do grupo do qual você deseja remover o membro.</span><span class="sxs-lookup"><span data-stu-id="2832c-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="2832c-126">-GroupObjectId</span></span>
<span data-ttu-id="2832c-127">A ID de objeto do grupo do qual você deseja remover o membro.</span><span class="sxs-lookup"><span data-stu-id="2832c-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="2832c-128">-MemberObjectId</span></span>
<span data-ttu-id="2832c-129">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="2832c-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2832c-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="2832c-131">O UPN do (s) membro (s) a remover.</span><span class="sxs-lookup"><span data-stu-id="2832c-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2832c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2832c-132">-PassThru</span></span>
<span data-ttu-id="2832c-133">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2832c-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2832c-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2832c-134">-Confirm</span></span>
<span data-ttu-id="2832c-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2832c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2832c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2832c-136">-WhatIf</span></span>
<span data-ttu-id="2832c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2832c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2832c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2832c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2832c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2832c-139">CommonParameters</span></span>
<span data-ttu-id="2832c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2832c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2832c-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2832c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2832c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2832c-142">INPUTS</span></span>

### <span data-ttu-id="2832c-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2832c-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="2832c-144">Parâmetros: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2832c-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="2832c-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2832c-145">OUTPUTS</span></span>

### <span data-ttu-id="2832c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2832c-146">System.Boolean</span></span>

## <span data-ttu-id="2832c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2832c-147">NOTES</span></span>

## <span data-ttu-id="2832c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2832c-148">RELATED LINKS</span></span>
