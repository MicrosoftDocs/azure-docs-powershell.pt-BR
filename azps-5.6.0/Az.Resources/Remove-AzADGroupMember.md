---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7cc64ad6d0f17666ac1e97ae00473907c53a5552
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885844"
---
# <span data-ttu-id="33a96-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="33a96-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="33a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a96-102">SYNOPSIS</span></span>
<span data-ttu-id="33a96-103">Remove um usuário de um grupo de AD.</span><span class="sxs-lookup"><span data-stu-id="33a96-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="33a96-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="33a96-104">SYNTAX</span></span>

### <span data-ttu-id="33a96-105">ExplicitParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="33a96-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33a96-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="33a96-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a96-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="33a96-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a96-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="33a96-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a96-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="33a96-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a96-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33a96-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a96-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33a96-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a96-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="33a96-112">DESCRIPTION</span></span>
<span data-ttu-id="33a96-113">Remove um usuário de um grupo de AD.</span><span class="sxs-lookup"><span data-stu-id="33a96-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="33a96-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33a96-114">EXAMPLES</span></span>

### <span data-ttu-id="33a96-115">Exemplo 1: Remover um usuário de um grupo por id de objeto</span><span class="sxs-lookup"><span data-stu-id="33a96-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="33a96-116">Remove o usuário com a id do objeto 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' do grupo com a id do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="33a96-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="33a96-117">Exemplo 2: Remover um usuário de um grupo canalização</span><span class="sxs-lookup"><span data-stu-id="33a96-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="33a96-118">Obtém o grupo com a id do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e canalizará-o para o cmdlet Remove-AzADGroupMember para remover o usuário para esse grupo.</span><span class="sxs-lookup"><span data-stu-id="33a96-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="33a96-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="33a96-119">PARAMETERS</span></span>

### <span data-ttu-id="33a96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a96-120">-DefaultProfile</span></span>
<span data-ttu-id="33a96-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33a96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a96-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="33a96-122">-GroupDisplayName</span></span>
<span data-ttu-id="33a96-123">O nome de exibição do grupo para remover os membros.</span><span class="sxs-lookup"><span data-stu-id="33a96-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="33a96-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="33a96-124">-GroupObject</span></span>
<span data-ttu-id="33a96-125">A representação de objeto do grupo de onde remover o membro.</span><span class="sxs-lookup"><span data-stu-id="33a96-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33a96-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="33a96-126">-GroupObjectId</span></span>
<span data-ttu-id="33a96-127">A ID do objeto do grupo para remover o membro.</span><span class="sxs-lookup"><span data-stu-id="33a96-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a96-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="33a96-128">-MemberObjectId</span></span>
<span data-ttu-id="33a96-129">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="33a96-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a96-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="33a96-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="33a96-131">O UPN dos membros a ser removido.</span><span class="sxs-lookup"><span data-stu-id="33a96-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="33a96-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33a96-132">-PassThru</span></span>
<span data-ttu-id="33a96-133">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="33a96-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="33a96-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33a96-134">-Confirm</span></span>
<span data-ttu-id="33a96-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a96-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a96-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a96-136">-WhatIf</span></span>
<span data-ttu-id="33a96-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33a96-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a96-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33a96-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a96-139">CommonParameters</span></span>
<span data-ttu-id="33a96-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a96-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33a96-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a96-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33a96-142">INPUTS</span></span>

### <span data-ttu-id="33a96-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="33a96-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="33a96-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="33a96-144">OUTPUTS</span></span>

### <span data-ttu-id="33a96-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33a96-145">System.Boolean</span></span>

## <span data-ttu-id="33a96-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="33a96-146">NOTES</span></span>

## <span data-ttu-id="33a96-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33a96-147">RELATED LINKS</span></span>
