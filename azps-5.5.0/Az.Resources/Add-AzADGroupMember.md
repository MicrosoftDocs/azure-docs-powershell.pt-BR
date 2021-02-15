---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114914"
---
# <span data-ttu-id="381a0-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="381a0-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="381a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="381a0-102">SYNOPSIS</span></span>
<span data-ttu-id="381a0-103">Adiciona um usuário a um grupo de AD existente.</span><span class="sxs-lookup"><span data-stu-id="381a0-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="381a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="381a0-104">SYNTAX</span></span>

### <span data-ttu-id="381a0-105">MemberObjectIdWithGroupObjectId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="381a0-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a0-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="381a0-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a0-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="381a0-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a0-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="381a0-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a0-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="381a0-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a0-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="381a0-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381a0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="381a0-111">DESCRIPTION</span></span>
<span data-ttu-id="381a0-112">Adiciona um usuário a um grupo de AD existente.</span><span class="sxs-lookup"><span data-stu-id="381a0-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="381a0-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="381a0-113">EXAMPLES</span></span>

### <span data-ttu-id="381a0-114">Exemplo 1: Adicionar um usuário a um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="381a0-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="381a0-115">Adiciona o usuário com a ID do objeto 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' ao grupo com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="381a0-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="381a0-116">Exemplo 2: Adicionar um usuário a um grupo por piping</span><span class="sxs-lookup"><span data-stu-id="381a0-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="381a0-117">Obtém o grupo com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e o canal no cmdlet Add-AzADGroupMember para adicionar o usuário a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="381a0-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="381a0-118">Exemplo 3: Adicionar um usuário a um grupo por nome principal</span><span class="sxs-lookup"><span data-stu-id="381a0-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="381a0-119">Adiciona um usuário a um grupo e lista os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="381a0-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="381a0-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="381a0-120">PARAMETERS</span></span>

### <span data-ttu-id="381a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381a0-121">-DefaultProfile</span></span>
<span data-ttu-id="381a0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="381a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="381a0-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="381a0-123">-MemberObjectId</span></span>
<span data-ttu-id="381a0-124">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="381a0-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381a0-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="381a0-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="381a0-126">O UPN dos membros a adicionar ao grupo.</span><span class="sxs-lookup"><span data-stu-id="381a0-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="381a0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="381a0-127">-PassThru</span></span>
<span data-ttu-id="381a0-128">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="381a0-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="381a0-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="381a0-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="381a0-130">O nome de exibição do grupo ao que adicionar os membros.</span><span class="sxs-lookup"><span data-stu-id="381a0-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="381a0-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="381a0-131">-TargetGroupObject</span></span>
<span data-ttu-id="381a0-132">A representação de objeto do grupo para adicionar os membros.</span><span class="sxs-lookup"><span data-stu-id="381a0-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="381a0-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="381a0-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="381a0-134">A ID do objeto do grupo para adicionar os membros.</span><span class="sxs-lookup"><span data-stu-id="381a0-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="381a0-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="381a0-135">-Confirm</span></span>
<span data-ttu-id="381a0-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381a0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="381a0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381a0-137">-WhatIf</span></span>
<span data-ttu-id="381a0-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="381a0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381a0-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="381a0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="381a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381a0-140">CommonParameters</span></span>
<span data-ttu-id="381a0-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381a0-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="381a0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381a0-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="381a0-143">INPUTS</span></span>

### <span data-ttu-id="381a0-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="381a0-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="381a0-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="381a0-145">OUTPUTS</span></span>

### <span data-ttu-id="381a0-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="381a0-146">System.Boolean</span></span>

## <span data-ttu-id="381a0-147">Notas</span><span class="sxs-lookup"><span data-stu-id="381a0-147">NOTES</span></span>

## <span data-ttu-id="381a0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="381a0-148">RELATED LINKS</span></span>
