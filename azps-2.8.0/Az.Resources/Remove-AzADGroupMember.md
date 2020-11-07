---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 1196480735705186ad3493b6c34a473baf35dc0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773327"
---
# <span data-ttu-id="f43f0-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f43f0-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="f43f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f43f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f43f0-103">Remove um usuário de um grupo do AD.</span><span class="sxs-lookup"><span data-stu-id="f43f0-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="f43f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f43f0-104">SYNTAX</span></span>

### <span data-ttu-id="f43f0-105">ExplicitParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f43f0-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f43f0-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="f43f0-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43f0-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="f43f0-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43f0-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="f43f0-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43f0-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f43f0-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43f0-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f43f0-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43f0-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f43f0-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f43f0-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f43f0-112">DESCRIPTION</span></span>
<span data-ttu-id="f43f0-113">Remove um usuário de um grupo do AD.</span><span class="sxs-lookup"><span data-stu-id="f43f0-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="f43f0-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f43f0-114">EXAMPLES</span></span>

### <span data-ttu-id="f43f0-115">Exemplo 1-remover um usuário de um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="f43f0-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f43f0-116">Remove o usuário com a ID de objeto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" do grupo com a ID de objeto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="f43f0-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f43f0-117">Exemplo 2-remover um usuário de um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="f43f0-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="f43f0-118">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e a canaliza para o cmdlet Remove-AzADGroupMember para remover o usuário desse grupo.</span><span class="sxs-lookup"><span data-stu-id="f43f0-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="f43f0-119">OS</span><span class="sxs-lookup"><span data-stu-id="f43f0-119">PARAMETERS</span></span>

### <span data-ttu-id="f43f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43f0-120">-DefaultProfile</span></span>
<span data-ttu-id="f43f0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f43f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f43f0-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="f43f0-122">-GroupDisplayName</span></span>
<span data-ttu-id="f43f0-123">O nome de exibição do grupo do qual você deseja remover o (s) membro (s).</span><span class="sxs-lookup"><span data-stu-id="f43f0-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="f43f0-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="f43f0-124">-GroupObject</span></span>
<span data-ttu-id="f43f0-125">A representação de objeto do grupo do qual você deseja remover o membro.</span><span class="sxs-lookup"><span data-stu-id="f43f0-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="f43f0-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="f43f0-126">-GroupObjectId</span></span>
<span data-ttu-id="f43f0-127">A ID de objeto do grupo do qual você deseja remover o membro.</span><span class="sxs-lookup"><span data-stu-id="f43f0-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="f43f0-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="f43f0-128">-MemberObjectId</span></span>
<span data-ttu-id="f43f0-129">A ID do objeto do membro.</span><span class="sxs-lookup"><span data-stu-id="f43f0-129">The object id of the member.</span></span>

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

### <span data-ttu-id="f43f0-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f43f0-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="f43f0-131">O UPN do (s) membro (s) a remover.</span><span class="sxs-lookup"><span data-stu-id="f43f0-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="f43f0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f43f0-132">-PassThru</span></span>
<span data-ttu-id="f43f0-133">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f43f0-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f43f0-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f43f0-134">-Confirm</span></span>
<span data-ttu-id="f43f0-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f43f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f43f0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43f0-136">-WhatIf</span></span>
<span data-ttu-id="f43f0-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f43f0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f43f0-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f43f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f43f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43f0-139">CommonParameters</span></span>
<span data-ttu-id="f43f0-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43f0-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f43f0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43f0-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f43f0-142">INPUTS</span></span>

### <span data-ttu-id="f43f0-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f43f0-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f43f0-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f43f0-144">OUTPUTS</span></span>

### <span data-ttu-id="f43f0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f43f0-145">System.Boolean</span></span>

## <span data-ttu-id="f43f0-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f43f0-146">NOTES</span></span>

## <span data-ttu-id="f43f0-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f43f0-147">RELATED LINKS</span></span>
