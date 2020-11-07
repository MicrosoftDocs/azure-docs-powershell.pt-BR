---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: f083498860f3f2b9e19280b41d953032796e0eb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776462"
---
# <span data-ttu-id="e44c6-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e44c6-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="e44c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e44c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e44c6-103">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e44c6-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="e44c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e44c6-104">SYNTAX</span></span>

### <span data-ttu-id="e44c6-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e44c6-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e44c6-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e44c6-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e44c6-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e44c6-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e44c6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e44c6-108">DESCRIPTION</span></span>
<span data-ttu-id="e44c6-109">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e44c6-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="e44c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e44c6-110">EXAMPLES</span></span>

### <span data-ttu-id="e44c6-111">Exemplo 1-listar Membros por ID de objeto do grupo AD</span><span class="sxs-lookup"><span data-stu-id="e44c6-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e44c6-112">Lista os membros do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="e44c6-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e44c6-113">Exemplo 2-listar Membros por ID de objeto do grupo AD usando paginação</span><span class="sxs-lookup"><span data-stu-id="e44c6-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="e44c6-114">Lista os primeiros membros do 100 do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="e44c6-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e44c6-115">Exemplo de 3-listar Membros por tubulação</span><span class="sxs-lookup"><span data-stu-id="e44c6-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="e44c6-116">Obtém o grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e o canaliza para o cmdlet Get-AzADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="e44c6-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="e44c6-117">OS</span><span class="sxs-lookup"><span data-stu-id="e44c6-117">PARAMETERS</span></span>

### <span data-ttu-id="e44c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44c6-118">-DefaultProfile</span></span>
<span data-ttu-id="e44c6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e44c6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e44c6-120">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="e44c6-120">-First</span></span>
<span data-ttu-id="e44c6-121">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="e44c6-121">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44c6-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e44c6-122">-GroupDisplayName</span></span>
<span data-ttu-id="e44c6-123">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="e44c6-123">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44c6-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="e44c6-124">-GroupObject</span></span>
<span data-ttu-id="e44c6-125">O objeto de grupo no qual você está listando os membros.</span><span class="sxs-lookup"><span data-stu-id="e44c6-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44c6-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e44c6-126">-GroupObjectId</span></span>
<span data-ttu-id="e44c6-127">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="e44c6-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e44c6-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e44c6-128">-IncludeTotalCount</span></span>
<span data-ttu-id="e44c6-129">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="e44c6-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e44c6-130">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="e44c6-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e44c6-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="e44c6-131">-Skip</span></span>
<span data-ttu-id="e44c6-132">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="e44c6-132">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44c6-133">CommonParameters</span></span>
<span data-ttu-id="e44c6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44c6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44c6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44c6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e44c6-136">INPUTS</span></span>

### <span data-ttu-id="e44c6-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e44c6-137">System.Guid</span></span>

### <span data-ttu-id="e44c6-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e44c6-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e44c6-139">Parâmetros: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e44c6-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="e44c6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e44c6-140">OUTPUTS</span></span>

### <span data-ttu-id="e44c6-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="e44c6-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="e44c6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e44c6-142">NOTES</span></span>

## <span data-ttu-id="e44c6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e44c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="e44c6-144">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e44c6-144">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="e44c6-145">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e44c6-145">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

