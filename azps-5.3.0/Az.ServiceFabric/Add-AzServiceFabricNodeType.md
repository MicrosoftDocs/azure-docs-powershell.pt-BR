---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433067"
---
# <span data-ttu-id="b772b-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="b772b-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="b772b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b772b-102">SYNOPSIS</span></span>
<span data-ttu-id="b772b-103">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="b772b-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="b772b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b772b-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b772b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b772b-105">DESCRIPTION</span></span>
<span data-ttu-id="b772b-106">Adicione um novo tipo de nó a um cluster existente.</span><span class="sxs-lookup"><span data-stu-id="b772b-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="b772b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b772b-107">EXAMPLES</span></span>

### <span data-ttu-id="b772b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b772b-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="b772b-109">Esse comando adicionará um novo NodeType ' N2 ' com capacidade de 5, e o nome do administrador da VM será ' adminname '.</span><span class="sxs-lookup"><span data-stu-id="b772b-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="b772b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b772b-110">PARAMETERS</span></span>

### <span data-ttu-id="b772b-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="b772b-111">-Capacity</span></span>
<span data-ttu-id="b772b-112">Capacidade</span><span class="sxs-lookup"><span data-stu-id="b772b-112">Capacity</span></span>

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

### <span data-ttu-id="b772b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b772b-113">-DefaultProfile</span></span>
<span data-ttu-id="b772b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b772b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b772b-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b772b-115">-DurabilityLevel</span></span>
<span data-ttu-id="b772b-116">Especifique o nível de durabilidade do NodeType.</span><span class="sxs-lookup"><span data-stu-id="b772b-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="b772b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b772b-117">-Name</span></span>
<span data-ttu-id="b772b-118">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="b772b-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b772b-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b772b-119">-NodeType</span></span>
<span data-ttu-id="b772b-120">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="b772b-120">The node type name</span></span>

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

### <span data-ttu-id="b772b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b772b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b772b-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b772b-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b772b-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="b772b-123">-Tier</span></span>
<span data-ttu-id="b772b-124">Camada SKU da VM</span><span class="sxs-lookup"><span data-stu-id="b772b-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="b772b-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b772b-125">-VmPassword</span></span>
<span data-ttu-id="b772b-126">A senha para fazer logon na VM</span><span class="sxs-lookup"><span data-stu-id="b772b-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="b772b-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b772b-127">-VmSku</span></span>
<span data-ttu-id="b772b-128">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="b772b-128">The sku name</span></span>

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

### <span data-ttu-id="b772b-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b772b-129">-VmUserName</span></span>
<span data-ttu-id="b772b-130">O nome de usuário para fazer logon na VM</span><span class="sxs-lookup"><span data-stu-id="b772b-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="b772b-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b772b-131">-Confirm</span></span>
<span data-ttu-id="b772b-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b772b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b772b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b772b-133">-WhatIf</span></span>
<span data-ttu-id="b772b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b772b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b772b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b772b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b772b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b772b-136">CommonParameters</span></span>
<span data-ttu-id="b772b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b772b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b772b-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b772b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b772b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b772b-139">INPUTS</span></span>

### <span data-ttu-id="b772b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b772b-140">System.String</span></span>

### <span data-ttu-id="b772b-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b772b-141">System.Int32</span></span>

### <span data-ttu-id="b772b-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b772b-142">System.Security.SecureString</span></span>

### <span data-ttu-id="b772b-143">Microsoft. Azure. Commands. imfabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b772b-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="b772b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b772b-144">OUTPUTS</span></span>

### <span data-ttu-id="b772b-145">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b772b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b772b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b772b-146">NOTES</span></span>

## <span data-ttu-id="b772b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b772b-147">RELATED LINKS</span></span>
