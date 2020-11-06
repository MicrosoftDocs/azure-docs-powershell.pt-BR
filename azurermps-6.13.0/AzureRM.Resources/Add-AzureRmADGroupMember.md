---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428386"
---
# <span data-ttu-id="7f2ae-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7f2ae-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="7f2ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2ae-103">Adiciona um usuário a um grupo de anúncios existente.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f2ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f2ae-104">SYNTAX</span></span>

### <span data-ttu-id="7f2ae-105">MemberObjectIdWithGroupObjectId (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f2ae-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2ae-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7f2ae-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2ae-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="7f2ae-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2ae-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2ae-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2ae-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2ae-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2ae-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2ae-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2ae-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f2ae-111">DESCRIPTION</span></span>
<span data-ttu-id="7f2ae-112">Adiciona um usuário a um grupo de anúncios existente.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="7f2ae-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f2ae-113">EXAMPLES</span></span>

### <span data-ttu-id="7f2ae-114">Exemplo 1-adicionar um usuário a um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="7f2ae-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="7f2ae-115">Adiciona o usuário com a ID de objeto ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' ao grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7f2ae-116">Exemplo 2-adicionar um usuário a um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="7f2ae-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="7f2ae-117">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e a canaliza para o cmdlet Add-AzureRmADGroupMember para adicionar o usuário ao grupo.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="7f2ae-118">OS</span><span class="sxs-lookup"><span data-stu-id="7f2ae-118">PARAMETERS</span></span>

### <span data-ttu-id="7f2ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2ae-119">-DefaultProfile</span></span>
<span data-ttu-id="7f2ae-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f2ae-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="7f2ae-121">-MemberObjectId</span></span>
<span data-ttu-id="7f2ae-122">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2ae-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7f2ae-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="7f2ae-124">O UPN do (s) membro (s) para adicionar ao grupo.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="7f2ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f2ae-125">-PassThru</span></span>
<span data-ttu-id="7f2ae-126">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7f2ae-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7f2ae-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="7f2ae-128">O nome de exibição do grupo ao qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="7f2ae-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7f2ae-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="7f2ae-129">-TargetGroupObject</span></span>
<span data-ttu-id="7f2ae-130">A representação de objeto do grupo para o qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="7f2ae-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7f2ae-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7f2ae-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="7f2ae-132">A ID de objeto do grupo ao qual adicionar o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="7f2ae-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7f2ae-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f2ae-133">-Confirm</span></span>
<span data-ttu-id="7f2ae-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2ae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2ae-135">-WhatIf</span></span>
<span data-ttu-id="7f2ae-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f2ae-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2ae-138">CommonParameters</span></span>
<span data-ttu-id="7f2ae-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2ae-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2ae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2ae-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f2ae-141">INPUTS</span></span>

### <span data-ttu-id="7f2ae-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="7f2ae-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="7f2ae-143">Parâmetros: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f2ae-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="7f2ae-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f2ae-144">OUTPUTS</span></span>

### <span data-ttu-id="7f2ae-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f2ae-145">System.Boolean</span></span>

## <span data-ttu-id="7f2ae-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f2ae-146">NOTES</span></span>

## <span data-ttu-id="7f2ae-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f2ae-147">RELATED LINKS</span></span>
