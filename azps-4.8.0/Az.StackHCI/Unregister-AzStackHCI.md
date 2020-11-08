---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113190"
---
# <span data-ttu-id="099fe-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="099fe-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="099fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="099fe-102">SYNOPSIS</span></span>
<span data-ttu-id="099fe-103">Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="099fe-104">As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.</span><span class="sxs-lookup"><span data-stu-id="099fe-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="099fe-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="099fe-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="099fe-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="099fe-106">DESCRIPTION</span></span>
<span data-ttu-id="099fe-107">Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="099fe-108">As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.</span><span class="sxs-lookup"><span data-stu-id="099fe-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="099fe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="099fe-109">EXAMPLES</span></span>

### <span data-ttu-id="099fe-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="099fe-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="099fe-111">C:\PS \> Unregister-AzStackHCI Result: Success</span><span class="sxs-lookup"><span data-stu-id="099fe-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="099fe-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="099fe-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="099fe-113">C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 Result: Success</span><span class="sxs-lookup"><span data-stu-id="099fe-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="099fe-114">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="099fe-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="099fe-115">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -ResourceId DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="099fe-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="099fe-116">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="099fe-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="099fe-117">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="099fe-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="099fe-118">OS</span><span class="sxs-lookup"><span data-stu-id="099fe-118">PARAMETERS</span></span>

### <span data-ttu-id="099fe-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="099fe-119">-SubscriptionId</span></span>
<span data-ttu-id="099fe-120">Especifica a assinatura do Azure para criar o recurso</span><span class="sxs-lookup"><span data-stu-id="099fe-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="099fe-121">-ResourceName</span></span>
<span data-ttu-id="099fe-122">Especifica o nome do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="099fe-123">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="099fe-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-124">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="099fe-124">-TenantId</span></span>
<span data-ttu-id="099fe-125">Especifica o Tenantid do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="099fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="099fe-127">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="099fe-128">Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="099fe-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="099fe-129">-ArmAccessToken</span></span>
<span data-ttu-id="099fe-130">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="099fe-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="099fe-131">Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="099fe-132">-GraphAccessToken</span></span>
<span data-ttu-id="099fe-133">Especifica o token de acesso do gráfico.</span><span class="sxs-lookup"><span data-stu-id="099fe-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="099fe-134">Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="099fe-135">-AccountId</span></span>
<span data-ttu-id="099fe-136">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="099fe-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="099fe-137">Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-138">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="099fe-138">-EnvironmentName</span></span>
<span data-ttu-id="099fe-139">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="099fe-140">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="099fe-140">Default is AzureCloud.</span></span>
<span data-ttu-id="099fe-141">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="099fe-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-142">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="099fe-142">-ComputerName</span></span>
<span data-ttu-id="099fe-143">Especifica um dos nós do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="099fe-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-144">-Credential</span><span class="sxs-lookup"><span data-stu-id="099fe-144">-Credential</span></span>
<span data-ttu-id="099fe-145">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="099fe-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="099fe-146">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="099fe-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099fe-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="099fe-147">-WhatIf</span></span>
<span data-ttu-id="099fe-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="099fe-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="099fe-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="099fe-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="099fe-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="099fe-150">-Confirm</span></span>
<span data-ttu-id="099fe-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="099fe-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="099fe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099fe-152">CommonParameters</span></span>
<span data-ttu-id="099fe-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099fe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099fe-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="099fe-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099fe-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="099fe-155">INPUTS</span></span>

## <span data-ttu-id="099fe-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="099fe-156">OUTPUTS</span></span>

### <span data-ttu-id="099fe-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="099fe-157">PSCustomObject.</span></span> <span data-ttu-id="099fe-158">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="099fe-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="099fe-159">Resultado: êxito ou falha ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="099fe-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="099fe-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="099fe-160">NOTES</span></span>

## <span data-ttu-id="099fe-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="099fe-161">RELATED LINKS</span></span>
