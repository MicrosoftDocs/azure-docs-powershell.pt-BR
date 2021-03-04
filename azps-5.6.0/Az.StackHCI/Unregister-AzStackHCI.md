---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888411"
---
# <span data-ttu-id="ca1e5-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="ca1e5-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="ca1e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1e5-103">Unregister-AzStackHCI exclui o recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e não registrou o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="ca1e5-104">As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="ca1e5-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca1e5-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca1e5-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca1e5-106">DESCRIPTION</span></span>
<span data-ttu-id="ca1e5-107">Unregister-AzStackHCI exclui o recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e não registrou o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="ca1e5-108">As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="ca1e5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-109">EXAMPLES</span></span>

### <span data-ttu-id="ca1e5-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ca1e5-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="ca1e5-111">Invocando em um dos nós de cluster</span><span class="sxs-lookup"><span data-stu-id="ca1e5-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="ca1e5-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="ca1e5-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="ca1e5-113">Invocando do nó de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ca1e5-113">Invoking from the management node</span></span>

### <span data-ttu-id="ca1e5-114">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="ca1e5-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="ca1e5-115">Invocando do WAC</span><span class="sxs-lookup"><span data-stu-id="ca1e5-115">Invoking from WAC</span></span>

### <span data-ttu-id="ca1e5-116">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="ca1e5-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="ca1e5-117">Invocando com todos os parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca1e5-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="ca1e5-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-118">PARAMETERS</span></span>

### <span data-ttu-id="ca1e5-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ca1e5-119">-AccountId</span></span>
<span data-ttu-id="ca1e5-120">Especifica o token de ARM de acesso.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="ca1e5-121">Especificar isso junto com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="ca1e5-122">-ArmAccessToken</span></span>
<span data-ttu-id="ca1e5-123">Especifica o token de ARM de acesso.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="ca1e5-124">Especificar isso junto com GraphAccessToken e AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ca1e5-125">-ComputerName</span></span>
<span data-ttu-id="ca1e5-126">Especifica um dos nós de cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="ca1e5-127">-Credential</span></span>
<span data-ttu-id="ca1e5-128">Especifica a credencial do ComputerName.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ca1e5-129">O padrão é o usuário atual executando o Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ca1e5-130">-EnvironmentName</span></span>
<span data-ttu-id="ca1e5-131">Especifica o Ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ca1e5-132">O padrão é o AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-132">Default is AzureCloud.</span></span>
<span data-ttu-id="ca1e5-133">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ca1e5-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ca1e5-134">-GraphAccessToken</span></span>
<span data-ttu-id="ca1e5-135">Especifica o token de acesso graph.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="ca1e5-136">Especificar isso junto com ArmAccessToken e AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1e5-137">-ResourceGroupName</span></span>
<span data-ttu-id="ca1e5-138">Especifica o nome do Grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="ca1e5-139">Se não especificado \<LocalClusterName\> -rg será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ca1e5-140">-ResourceName</span></span>
<span data-ttu-id="ca1e5-141">Especifica o nome do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="ca1e5-142">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca1e5-143">-SubscriptionId</span></span>
<span data-ttu-id="ca1e5-144">Especifica a Assinatura do Azure para criar o recurso</span><span class="sxs-lookup"><span data-stu-id="ca1e5-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ca1e5-145">-TenantId</span></span>
<span data-ttu-id="ca1e5-146">Especifica o TenantId do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ca1e5-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="ca1e5-148">Use a autenticação de código de dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1e5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca1e5-149">-Confirm</span></span>
<span data-ttu-id="ca1e5-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1e5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1e5-151">-WhatIf</span></span>
<span data-ttu-id="ca1e5-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1e5-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1e5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1e5-154">CommonParameters</span></span>
<span data-ttu-id="ca1e5-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1e5-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca1e5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1e5-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-157">INPUTS</span></span>

## <span data-ttu-id="ca1e5-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-158">OUTPUTS</span></span>

### <span data-ttu-id="ca1e5-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-159">PSCustomObject.</span></span> <span data-ttu-id="ca1e5-160">Retorna propriedades a seguir em PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="ca1e5-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ca1e5-161">Resultado: Êxito ou Falha ou Cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ca1e5-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="ca1e5-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca1e5-162">NOTES</span></span>

## <span data-ttu-id="ca1e5-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca1e5-163">RELATED LINKS</span></span>
