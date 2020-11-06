---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 25de035b853d1a17ee06a7efb6ac31631bd466f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599453"
---
# <span data-ttu-id="1ba39-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="1ba39-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="1ba39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ba39-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba39-103">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="1ba39-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="1ba39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba39-104">SYNTAX</span></span>

### <span data-ttu-id="1ba39-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ba39-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1ba39-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba39-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1ba39-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba39-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1ba39-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ba39-108">DESCRIPTION</span></span>
<span data-ttu-id="1ba39-109">Lista os membros de um grupo de anúncios no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="1ba39-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="1ba39-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ba39-110">EXAMPLES</span></span>

### <span data-ttu-id="1ba39-111">Exemplo 1-listar Membros por ID de objeto do grupo AD</span><span class="sxs-lookup"><span data-stu-id="1ba39-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="1ba39-112">Lista os membros do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="1ba39-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="1ba39-113">Exemplo 2-listar Membros por ID de objeto do grupo AD usando paginação</span><span class="sxs-lookup"><span data-stu-id="1ba39-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="1ba39-114">Lista os primeiros membros do 100 do grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="1ba39-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="1ba39-115">Exemplo de 3-listar Membros por tubulação</span><span class="sxs-lookup"><span data-stu-id="1ba39-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="1ba39-116">Obtém o grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e o canaliza para o cmdlet Get-AzADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="1ba39-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="1ba39-117">OS</span><span class="sxs-lookup"><span data-stu-id="1ba39-117">PARAMETERS</span></span>

### <span data-ttu-id="1ba39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba39-118">-DefaultProfile</span></span>
<span data-ttu-id="1ba39-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1ba39-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ba39-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="1ba39-120">-GroupDisplayName</span></span>
<span data-ttu-id="1ba39-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="1ba39-121">The display name of the group.</span></span>

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

### <span data-ttu-id="1ba39-122">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="1ba39-122">-GroupObject</span></span>
<span data-ttu-id="1ba39-123">O objeto de grupo no qual você está listando os membros.</span><span class="sxs-lookup"><span data-stu-id="1ba39-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba39-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="1ba39-124">-GroupObjectId</span></span>
<span data-ttu-id="1ba39-125">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="1ba39-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba39-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1ba39-126">-IncludeTotalCount</span></span>
<span data-ttu-id="1ba39-127">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="1ba39-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1ba39-128">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="1ba39-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1ba39-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="1ba39-129">-Skip</span></span>
<span data-ttu-id="1ba39-130">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="1ba39-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1ba39-131">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="1ba39-131">-First</span></span>
<span data-ttu-id="1ba39-132">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="1ba39-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1ba39-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba39-133">CommonParameters</span></span>
<span data-ttu-id="1ba39-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba39-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba39-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba39-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba39-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ba39-136">INPUTS</span></span>

### <span data-ttu-id="1ba39-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1ba39-137">System.String</span></span>

### <span data-ttu-id="1ba39-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="1ba39-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="1ba39-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ba39-139">OUTPUTS</span></span>

### <span data-ttu-id="1ba39-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="1ba39-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="1ba39-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ba39-141">NOTES</span></span>

## <span data-ttu-id="1ba39-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ba39-142">RELATED LINKS</span></span>

[<span data-ttu-id="1ba39-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1ba39-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="1ba39-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1ba39-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

