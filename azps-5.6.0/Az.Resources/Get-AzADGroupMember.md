---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: d351ee85c36b9f5f8493879cded058fd7220450f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889762"
---
# <span data-ttu-id="739b3-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="739b3-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="739b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="739b3-102">SYNOPSIS</span></span>
<span data-ttu-id="739b3-103">Lista membros de um grupo de AD no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="739b3-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="739b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="739b3-104">SYNTAX</span></span>

### <span data-ttu-id="739b3-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="739b3-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="739b3-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="739b3-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="739b3-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="739b3-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="739b3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="739b3-108">DESCRIPTION</span></span>
<span data-ttu-id="739b3-109">Lista membros de um grupo de AD no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="739b3-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="739b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="739b3-110">EXAMPLES</span></span>

### <span data-ttu-id="739b3-111">Exemplo 1: Listar membros por ID de objeto de grupo do AD</span><span class="sxs-lookup"><span data-stu-id="739b3-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="739b3-112">Lista os membros do grupo AD com a id do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="739b3-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="739b3-113">Exemplo 2: Listar membros por ID de objeto de grupo do AD usando paging</span><span class="sxs-lookup"><span data-stu-id="739b3-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="739b3-114">Lista os primeiros 100 membros do grupo do AD com a id do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="739b3-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="739b3-115">Exemplo 3: Listar membros por canalização</span><span class="sxs-lookup"><span data-stu-id="739b3-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="739b3-116">Obtém o grupo AD com a id do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e canalizará-o para o cmdlet Get-AzADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="739b3-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="739b3-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="739b3-117">PARAMETERS</span></span>

### <span data-ttu-id="739b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739b3-118">-DefaultProfile</span></span>
<span data-ttu-id="739b3-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="739b3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="739b3-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="739b3-120">-GroupDisplayName</span></span>
<span data-ttu-id="739b3-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="739b3-121">The display name of the group.</span></span>

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

### <span data-ttu-id="739b3-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="739b3-122">-GroupObject</span></span>
<span data-ttu-id="739b3-123">O objeto group do que você está listando membros.</span><span class="sxs-lookup"><span data-stu-id="739b3-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="739b3-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="739b3-124">-GroupObjectId</span></span>
<span data-ttu-id="739b3-125">ID do objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="739b3-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="739b3-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="739b3-126">-IncludeTotalCount</span></span>
<span data-ttu-id="739b3-127">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="739b3-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="739b3-128">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="739b3-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="739b3-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="739b3-129">-Skip</span></span>
<span data-ttu-id="739b3-130">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="739b3-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="739b3-131">-First</span><span class="sxs-lookup"><span data-stu-id="739b3-131">-First</span></span>
<span data-ttu-id="739b3-132">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="739b3-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="739b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739b3-133">CommonParameters</span></span>
<span data-ttu-id="739b3-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="739b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739b3-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="739b3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739b3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="739b3-136">INPUTS</span></span>

### <span data-ttu-id="739b3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="739b3-137">System.String</span></span>

### <span data-ttu-id="739b3-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="739b3-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="739b3-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="739b3-139">OUTPUTS</span></span>

### <span data-ttu-id="739b3-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="739b3-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="739b3-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="739b3-141">NOTES</span></span>

## <span data-ttu-id="739b3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="739b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="739b3-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="739b3-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="739b3-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="739b3-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

