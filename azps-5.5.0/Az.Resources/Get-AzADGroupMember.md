---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111442"
---
# <span data-ttu-id="6ec38-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="6ec38-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="6ec38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ec38-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec38-103">Lista os membros de um grupo de AD no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="6ec38-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="6ec38-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ec38-104">SYNTAX</span></span>

### <span data-ttu-id="6ec38-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6ec38-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6ec38-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ec38-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6ec38-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ec38-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="6ec38-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ec38-108">DESCRIPTION</span></span>
<span data-ttu-id="6ec38-109">Lista os membros de um grupo de AD no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="6ec38-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="6ec38-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ec38-110">EXAMPLES</span></span>

### <span data-ttu-id="6ec38-111">Exemplo 1: Membros da lista por ID do objeto do grupo AD</span><span class="sxs-lookup"><span data-stu-id="6ec38-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6ec38-112">Lista os membros do grupo AD com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="6ec38-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="6ec38-113">Exemplo 2: Listar membros por ID de objeto de grupo AD usando paging</span><span class="sxs-lookup"><span data-stu-id="6ec38-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="6ec38-114">Lista os primeiros 100 membros do grupo AD com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="6ec38-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="6ec38-115">Exemplo 3: Listar membros por piping</span><span class="sxs-lookup"><span data-stu-id="6ec38-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="6ec38-116">Obtém o grupo AD com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e o canal no cmdlet Get-AzADGroupMember para listar todos os membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="6ec38-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="6ec38-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ec38-117">PARAMETERS</span></span>

### <span data-ttu-id="6ec38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec38-118">-DefaultProfile</span></span>
<span data-ttu-id="6ec38-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6ec38-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ec38-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ec38-120">-GroupDisplayName</span></span>
<span data-ttu-id="6ec38-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="6ec38-121">The display name of the group.</span></span>

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

### <span data-ttu-id="6ec38-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="6ec38-122">-GroupObject</span></span>
<span data-ttu-id="6ec38-123">O objeto do grupo do que você está listando membros.</span><span class="sxs-lookup"><span data-stu-id="6ec38-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="6ec38-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="6ec38-124">-GroupObjectId</span></span>
<span data-ttu-id="6ec38-125">ID do objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="6ec38-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="6ec38-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6ec38-126">-IncludeTotalCount</span></span>
<span data-ttu-id="6ec38-127">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="6ec38-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="6ec38-128">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="6ec38-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="6ec38-129">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="6ec38-129">-Skip</span></span>
<span data-ttu-id="6ec38-130">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="6ec38-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6ec38-131">-First</span><span class="sxs-lookup"><span data-stu-id="6ec38-131">-First</span></span>
<span data-ttu-id="6ec38-132">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="6ec38-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="6ec38-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec38-133">CommonParameters</span></span>
<span data-ttu-id="6ec38-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec38-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec38-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ec38-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec38-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="6ec38-136">INPUTS</span></span>

### <span data-ttu-id="6ec38-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6ec38-137">System.String</span></span>

### <span data-ttu-id="6ec38-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="6ec38-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="6ec38-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="6ec38-139">OUTPUTS</span></span>

### <span data-ttu-id="6ec38-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="6ec38-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="6ec38-141">Notas</span><span class="sxs-lookup"><span data-stu-id="6ec38-141">NOTES</span></span>

## <span data-ttu-id="6ec38-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ec38-142">RELATED LINKS</span></span>

[<span data-ttu-id="6ec38-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6ec38-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="6ec38-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ec38-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

