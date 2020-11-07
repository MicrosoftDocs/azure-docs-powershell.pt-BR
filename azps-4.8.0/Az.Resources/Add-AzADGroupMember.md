---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948063"
---
# <span data-ttu-id="2c745-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="2c745-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="2c745-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c745-102">SYNOPSIS</span></span>
<span data-ttu-id="2c745-103">Adiciona um usuário a um grupo de anúncios existente.</span><span class="sxs-lookup"><span data-stu-id="2c745-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2c745-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c745-104">SYNTAX</span></span>

### <span data-ttu-id="2c745-105">MemberObjectIdWithGroupObjectId (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c745-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c745-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2c745-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c745-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c745-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c745-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c745-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c745-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c745-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c745-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c745-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c745-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c745-111">DESCRIPTION</span></span>
<span data-ttu-id="2c745-112">Adiciona um usuário a um grupo de anúncios existente.</span><span class="sxs-lookup"><span data-stu-id="2c745-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2c745-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c745-113">EXAMPLES</span></span>

### <span data-ttu-id="2c745-114">Exemplo 1: adicionar um usuário a um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="2c745-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="2c745-115">Adiciona o usuário com a ID de objeto ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' ao grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="2c745-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="2c745-116">Exemplo 2: adicionar um usuário a um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="2c745-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="2c745-117">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e a canaliza para o cmdlet Add-AzADGroupMember para adicionar o usuário ao grupo.</span><span class="sxs-lookup"><span data-stu-id="2c745-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="2c745-118">Exemplo 3: adicionar um usuário a um grupo por nome principal</span><span class="sxs-lookup"><span data-stu-id="2c745-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="2c745-119">Adiciona um usuário a um grupo e lista os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="2c745-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="2c745-120">OS</span><span class="sxs-lookup"><span data-stu-id="2c745-120">PARAMETERS</span></span>

### <span data-ttu-id="2c745-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c745-121">-DefaultProfile</span></span>
<span data-ttu-id="2c745-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c745-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c745-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="2c745-123">-MemberObjectId</span></span>
<span data-ttu-id="2c745-124">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="2c745-124">The object id of the member.</span></span>

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

### <span data-ttu-id="2c745-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2c745-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="2c745-126">O UPN do (s) membro (s) para adicionar ao grupo.</span><span class="sxs-lookup"><span data-stu-id="2c745-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="2c745-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c745-127">-PassThru</span></span>
<span data-ttu-id="2c745-128">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2c745-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2c745-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2c745-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="2c745-130">O nome de exibição do grupo ao qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="2c745-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2c745-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c745-131">-TargetGroupObject</span></span>
<span data-ttu-id="2c745-132">A representação de objeto do grupo para o qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="2c745-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2c745-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="2c745-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="2c745-134">A ID de objeto do grupo ao qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="2c745-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2c745-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c745-135">-Confirm</span></span>
<span data-ttu-id="2c745-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c745-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c745-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c745-137">-WhatIf</span></span>
<span data-ttu-id="2c745-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c745-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c745-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c745-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c745-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c745-140">CommonParameters</span></span>
<span data-ttu-id="2c745-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c745-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c745-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c745-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c745-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c745-143">INPUTS</span></span>

### <span data-ttu-id="2c745-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2c745-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2c745-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c745-145">OUTPUTS</span></span>

### <span data-ttu-id="2c745-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c745-146">System.Boolean</span></span>

## <span data-ttu-id="2c745-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c745-147">NOTES</span></span>

## <span data-ttu-id="2c745-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c745-148">RELATED LINKS</span></span>
