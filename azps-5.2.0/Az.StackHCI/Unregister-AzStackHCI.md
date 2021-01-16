---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261030"
---
# <span data-ttu-id="607e9-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="607e9-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="607e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="607e9-102">SYNOPSIS</span></span>
<span data-ttu-id="607e9-103">Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="607e9-104">As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.</span><span class="sxs-lookup"><span data-stu-id="607e9-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="607e9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="607e9-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607e9-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="607e9-106">DESCRIPTION</span></span>
<span data-ttu-id="607e9-107">Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="607e9-108">As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.</span><span class="sxs-lookup"><span data-stu-id="607e9-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="607e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="607e9-109">EXAMPLES</span></span>

### <span data-ttu-id="607e9-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="607e9-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="607e9-111">C:\PS \> Unregister-AzStackHCI Result: Success</span><span class="sxs-lookup"><span data-stu-id="607e9-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="607e9-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="607e9-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="607e9-113">C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 Result: Success</span><span class="sxs-lookup"><span data-stu-id="607e9-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="607e9-114">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="607e9-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="607e9-115">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -ResourceId DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="607e9-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="607e9-116">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="607e9-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="607e9-117">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="607e9-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="607e9-118">OS</span><span class="sxs-lookup"><span data-stu-id="607e9-118">PARAMETERS</span></span>

### <span data-ttu-id="607e9-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="607e9-119">-AccountId</span></span>
<span data-ttu-id="607e9-120">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="607e9-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="607e9-121">Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="607e9-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="607e9-122">-ArmAccessToken</span></span>
<span data-ttu-id="607e9-123">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="607e9-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="607e9-124">Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="607e9-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="607e9-125">-ComputerName</span></span>
<span data-ttu-id="607e9-126">Especifica um dos nós do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="607e9-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="607e9-127">-Credential</span></span>
<span data-ttu-id="607e9-128">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="607e9-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="607e9-129">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="607e9-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="607e9-130">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="607e9-130">-EnvironmentName</span></span>
<span data-ttu-id="607e9-131">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="607e9-132">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="607e9-132">Default is AzureCloud.</span></span>
<span data-ttu-id="607e9-133">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="607e9-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="607e9-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="607e9-134">-GraphAccessToken</span></span>
<span data-ttu-id="607e9-135">Especifica o token de acesso do gráfico.</span><span class="sxs-lookup"><span data-stu-id="607e9-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="607e9-136">Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="607e9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607e9-137">-ResourceGroupName</span></span>
<span data-ttu-id="607e9-138">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="607e9-139">Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="607e9-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="607e9-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="607e9-140">-ResourceName</span></span>
<span data-ttu-id="607e9-141">Especifica o nome do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="607e9-142">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="607e9-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="607e9-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="607e9-143">-SubscriptionId</span></span>
<span data-ttu-id="607e9-144">Especifica a assinatura do Azure para criar o recurso</span><span class="sxs-lookup"><span data-stu-id="607e9-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="607e9-145">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="607e9-145">-TenantId</span></span>
<span data-ttu-id="607e9-146">Especifica o Tenantid do Azure.</span><span class="sxs-lookup"><span data-stu-id="607e9-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="607e9-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="607e9-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="607e9-148">Use a autenticação de código do dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="607e9-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="607e9-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="607e9-149">-Confirm</span></span>
<span data-ttu-id="607e9-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="607e9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607e9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607e9-151">-WhatIf</span></span>
<span data-ttu-id="607e9-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="607e9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607e9-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="607e9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607e9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607e9-154">CommonParameters</span></span>
<span data-ttu-id="607e9-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607e9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607e9-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="607e9-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607e9-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="607e9-157">INPUTS</span></span>

## <span data-ttu-id="607e9-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="607e9-158">OUTPUTS</span></span>

### <span data-ttu-id="607e9-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="607e9-159">PSCustomObject.</span></span> <span data-ttu-id="607e9-160">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="607e9-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="607e9-161">Resultado: êxito ou falha ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="607e9-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="607e9-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="607e9-162">NOTES</span></span>

## <span data-ttu-id="607e9-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="607e9-163">RELATED LINKS</span></span>
