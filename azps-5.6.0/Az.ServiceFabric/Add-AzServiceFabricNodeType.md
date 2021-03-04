---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: aef628c121fa01cf07b0c70764b7d34ac10f259a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886581"
---
# <span data-ttu-id="12888-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="12888-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="12888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12888-102">SYNOPSIS</span></span>
<span data-ttu-id="12888-103">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="12888-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="12888-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12888-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12888-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12888-105">DESCRIPTION</span></span>
<span data-ttu-id="12888-106">Adicione um novo tipo de nó a um cluster existente.</span><span class="sxs-lookup"><span data-stu-id="12888-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="12888-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12888-107">EXAMPLES</span></span>

### <span data-ttu-id="12888-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12888-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="12888-109">Este comando adicionará um novo NodeType 'n2' com capacidade de 5, e o nome de administrador do vm é 'adminName'.</span><span class="sxs-lookup"><span data-stu-id="12888-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="12888-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12888-110">PARAMETERS</span></span>

### <span data-ttu-id="12888-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="12888-111">-Capacity</span></span>
<span data-ttu-id="12888-112">Capacidade</span><span class="sxs-lookup"><span data-stu-id="12888-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12888-113">-DefaultProfile</span></span>
<span data-ttu-id="12888-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12888-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12888-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12888-115">-DurabilityLevel</span></span>
<span data-ttu-id="12888-116">Especifique o nível de durabilidade do NodeType.</span><span class="sxs-lookup"><span data-stu-id="12888-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12888-117">-Name</span></span>
<span data-ttu-id="12888-118">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="12888-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="12888-119">-NodeType</span></span>
<span data-ttu-id="12888-120">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="12888-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12888-121">-ResourceGroupName</span></span>
<span data-ttu-id="12888-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12888-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="12888-123">-Tier</span></span>
<span data-ttu-id="12888-124">Camada Vm Sku</span><span class="sxs-lookup"><span data-stu-id="12888-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="12888-125">-VmPassword</span></span>
<span data-ttu-id="12888-126">A senha para logon no Vm</span><span class="sxs-lookup"><span data-stu-id="12888-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="12888-127">-VmSku</span></span>
<span data-ttu-id="12888-128">O nome sku</span><span class="sxs-lookup"><span data-stu-id="12888-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="12888-129">-VmUserName</span></span>
<span data-ttu-id="12888-130">O nome de usuário para o log em Vm</span><span class="sxs-lookup"><span data-stu-id="12888-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12888-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12888-131">-Confirm</span></span>
<span data-ttu-id="12888-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12888-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12888-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12888-133">-WhatIf</span></span>
<span data-ttu-id="12888-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12888-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12888-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12888-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12888-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12888-136">CommonParameters</span></span>
<span data-ttu-id="12888-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12888-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12888-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12888-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12888-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12888-139">INPUTS</span></span>

### <span data-ttu-id="12888-140">System.String</span><span class="sxs-lookup"><span data-stu-id="12888-140">System.String</span></span>

### <span data-ttu-id="12888-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="12888-141">System.Int32</span></span>

### <span data-ttu-id="12888-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="12888-142">System.Security.SecureString</span></span>

### <span data-ttu-id="12888-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12888-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="12888-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12888-144">OUTPUTS</span></span>

### <span data-ttu-id="12888-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="12888-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12888-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="12888-146">NOTES</span></span>

## <span data-ttu-id="12888-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12888-147">RELATED LINKS</span></span>
