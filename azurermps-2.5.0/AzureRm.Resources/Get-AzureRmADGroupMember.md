---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: f790266f1e61446cb9d1c257929cf8b6e3ab25d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785629"
---
# <span data-ttu-id="827c4-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="827c4-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="827c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="827c4-102">SYNOPSIS</span></span>
<span data-ttu-id="827c4-103">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="827c4-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="827c4-104">SYNTAX</span></span>

### <span data-ttu-id="827c4-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="827c4-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="827c4-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="827c4-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="827c4-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="827c4-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="827c4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="827c4-108">DESCRIPTION</span></span>
<span data-ttu-id="827c4-109">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="827c4-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="827c4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="827c4-110">EXAMPLES</span></span>

### <span data-ttu-id="827c4-111">Exemplo 1-listar Membros por ID de objeto do grupo AD</span><span class="sxs-lookup"><span data-stu-id="827c4-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="827c4-112">Lista os membros do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="827c4-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="827c4-113">Exemplo 2-listar Membros por ID de objeto do grupo AD usando paginação</span><span class="sxs-lookup"><span data-stu-id="827c4-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="827c4-114">Lista os primeiros membros do 100 do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="827c4-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="827c4-115">Exemplo de 3-listar Membros por tubulação</span><span class="sxs-lookup"><span data-stu-id="827c4-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="827c4-116">Obtém o grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e o canaliza para o cmdlet Get-AzureRmADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="827c4-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="827c4-117">OS</span><span class="sxs-lookup"><span data-stu-id="827c4-117">PARAMETERS</span></span>

### <span data-ttu-id="827c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827c4-118">-DefaultProfile</span></span>
<span data-ttu-id="827c4-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="827c4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="827c4-120">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="827c4-120">-First</span></span>
<span data-ttu-id="827c4-121">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="827c4-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="827c4-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="827c4-122">-GroupDisplayName</span></span>
<span data-ttu-id="827c4-123">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="827c4-123">The display name of the group.</span></span>

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

### <span data-ttu-id="827c4-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="827c4-124">-GroupObject</span></span>
<span data-ttu-id="827c4-125">O objeto de grupo no qual você está listando os membros.</span><span class="sxs-lookup"><span data-stu-id="827c4-125">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="827c4-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="827c4-126">-GroupObjectId</span></span>
<span data-ttu-id="827c4-127">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="827c4-127">Object Id of the group.</span></span>

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

### <span data-ttu-id="827c4-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="827c4-128">-IncludeTotalCount</span></span>
<span data-ttu-id="827c4-129">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="827c4-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="827c4-130">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="827c4-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="827c4-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="827c4-131">-Skip</span></span>
<span data-ttu-id="827c4-132">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="827c4-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="827c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827c4-133">CommonParameters</span></span>
<span data-ttu-id="827c4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827c4-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827c4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827c4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="827c4-136">INPUTS</span></span>

### <span data-ttu-id="827c4-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="827c4-137">System.Guid</span></span>

### <span data-ttu-id="827c4-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="827c4-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="827c4-139">Parâmetros: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="827c4-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="827c4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="827c4-140">OUTPUTS</span></span>

### <span data-ttu-id="827c4-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="827c4-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="827c4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="827c4-142">NOTES</span></span>

## <span data-ttu-id="827c4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="827c4-143">RELATED LINKS</span></span>

[<span data-ttu-id="827c4-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="827c4-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="827c4-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="827c4-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

