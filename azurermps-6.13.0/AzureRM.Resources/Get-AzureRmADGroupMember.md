---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441446"
---
# <span data-ttu-id="e6b85-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e6b85-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="e6b85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6b85-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b85-103">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e6b85-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6b85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6b85-104">SYNTAX</span></span>

### <span data-ttu-id="e6b85-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6b85-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e6b85-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b85-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e6b85-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b85-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e6b85-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6b85-108">DESCRIPTION</span></span>
<span data-ttu-id="e6b85-109">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e6b85-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="e6b85-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6b85-110">EXAMPLES</span></span>

### <span data-ttu-id="e6b85-111">Exemplo 1-listar Membros por ID de objeto do grupo AD</span><span class="sxs-lookup"><span data-stu-id="e6b85-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e6b85-112">Lista os membros do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="e6b85-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e6b85-113">Exemplo 2-listar Membros por ID de objeto do grupo AD usando paginação</span><span class="sxs-lookup"><span data-stu-id="e6b85-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="e6b85-114">Lista os primeiros membros do 100 do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="e6b85-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e6b85-115">Exemplo de 3-listar Membros por tubulação</span><span class="sxs-lookup"><span data-stu-id="e6b85-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="e6b85-116">Obtém o grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e o canaliza para o cmdlet Get-AzureRmADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="e6b85-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="e6b85-117">OS</span><span class="sxs-lookup"><span data-stu-id="e6b85-117">PARAMETERS</span></span>

### <span data-ttu-id="e6b85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b85-118">-DefaultProfile</span></span>
<span data-ttu-id="e6b85-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e6b85-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6b85-120">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="e6b85-120">-First</span></span>
<span data-ttu-id="e6b85-121">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="e6b85-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e6b85-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e6b85-122">-GroupDisplayName</span></span>
<span data-ttu-id="e6b85-123">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="e6b85-123">The display name of the group.</span></span>

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

### <span data-ttu-id="e6b85-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="e6b85-124">-GroupObject</span></span>
<span data-ttu-id="e6b85-125">O objeto de grupo no qual você está listando os membros.</span><span class="sxs-lookup"><span data-stu-id="e6b85-125">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="e6b85-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e6b85-126">-GroupObjectId</span></span>
<span data-ttu-id="e6b85-127">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="e6b85-127">Object Id of the group.</span></span>

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

### <span data-ttu-id="e6b85-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e6b85-128">-IncludeTotalCount</span></span>
<span data-ttu-id="e6b85-129">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="e6b85-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e6b85-130">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="e6b85-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e6b85-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="e6b85-131">-Skip</span></span>
<span data-ttu-id="e6b85-132">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="e6b85-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e6b85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b85-133">CommonParameters</span></span>
<span data-ttu-id="e6b85-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b85-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b85-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b85-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6b85-136">INPUTS</span></span>

### <span data-ttu-id="e6b85-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e6b85-137">System.Guid</span></span>

### <span data-ttu-id="e6b85-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e6b85-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e6b85-139">Parâmetros: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6b85-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="e6b85-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6b85-140">OUTPUTS</span></span>

### <span data-ttu-id="e6b85-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="e6b85-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="e6b85-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6b85-142">NOTES</span></span>

## <span data-ttu-id="e6b85-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6b85-143">RELATED LINKS</span></span>

[<span data-ttu-id="e6b85-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e6b85-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="e6b85-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e6b85-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

