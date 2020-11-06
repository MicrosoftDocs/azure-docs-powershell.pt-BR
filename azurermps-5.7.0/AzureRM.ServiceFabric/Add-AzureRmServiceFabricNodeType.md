---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427438"
---
# <span data-ttu-id="1e0fe-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1e0fe-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="1e0fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0fe-103">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e0fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e0fe-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e0fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e0fe-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0fe-106">Adicione um novo tipo de nó a um cluster existente.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="1e0fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e0fe-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e0fe-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="1e0fe-109">Esse comando adicionará um novo NodeType ' N2 ' com capacidade de 5, e o nome do administrador da VM será ' adminname '.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="1e0fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="1e0fe-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0fe-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="1e0fe-111">-Capacity</span></span>
<span data-ttu-id="1e0fe-112">Capacidade</span><span class="sxs-lookup"><span data-stu-id="1e0fe-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0fe-113">-DefaultProfile</span></span>
<span data-ttu-id="1e0fe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="1e0fe-115">-DurabilityLevel</span></span>
<span data-ttu-id="1e0fe-116">Especifique o nível de durabilidade do NodeType.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e0fe-117">-Name</span></span>
<span data-ttu-id="1e0fe-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1e0fe-119">-NodeType</span></span>
<span data-ttu-id="1e0fe-120">O nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e0fe-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-122">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="1e0fe-123">-Tier</span></span>
<span data-ttu-id="1e0fe-124">Camada SKU da VM.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="1e0fe-125">-VmPassword</span></span>
<span data-ttu-id="1e0fe-126">A senha de login para a VM.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="1e0fe-127">-VmSku</span></span>
<span data-ttu-id="1e0fe-128">O nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-129">-VmUserName</span></span>
<span data-ttu-id="1e0fe-130">O nome de usuário para logon na VM.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e0fe-131">-Confirm</span></span>
<span data-ttu-id="1e0fe-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0fe-133">-WhatIf</span></span>
<span data-ttu-id="1e0fe-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e0fe-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0fe-136">CommonParameters</span></span>
<span data-ttu-id="1e0fe-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0fe-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e0fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0fe-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e0fe-139">INPUTS</span></span>

### <span data-ttu-id="1e0fe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1e0fe-140">System.String</span></span>
<span data-ttu-id="1e0fe-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1e0fe-141">System.Int32</span></span>

## <span data-ttu-id="1e0fe-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e0fe-142">OUTPUTS</span></span>

### <span data-ttu-id="1e0fe-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e0fe-143">System.Object</span></span>

## <span data-ttu-id="1e0fe-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e0fe-144">NOTES</span></span>

## <span data-ttu-id="1e0fe-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e0fe-145">RELATED LINKS</span></span>

