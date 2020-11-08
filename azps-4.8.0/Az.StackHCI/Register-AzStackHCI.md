---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113191"
---
# <span data-ttu-id="0e507-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="0e507-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="0e507-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e507-102">SYNOPSIS</span></span>
<span data-ttu-id="0e507-103">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="0e507-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e507-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="0e507-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e507-105">DESCRIPTION</span></span>
<span data-ttu-id="0e507-106">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="0e507-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e507-107">EXAMPLES</span></span>

### <span data-ttu-id="0e507-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="0e507-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="0e507-109">\>Registro C:\PS-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" resultado: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL:https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="0e507-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="0e507-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="0e507-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="0e507-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-NomeDoComputador ClusterNode1 Result: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="0e507-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="0e507-112">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="0e507-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="0e507-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="0e507-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="0e507-114">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="0e507-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="0e507-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region oesteus-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="0e507-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="0e507-116">OS</span><span class="sxs-lookup"><span data-stu-id="0e507-116">PARAMETERS</span></span>

### <span data-ttu-id="0e507-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e507-117">-SubscriptionId</span></span>
<span data-ttu-id="0e507-118">Especifica a assinatura do Azure para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="0e507-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="0e507-119">Esse é o único parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0e507-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e507-120">-Região</span><span class="sxs-lookup"><span data-stu-id="0e507-120">-Region</span></span>
<span data-ttu-id="0e507-121">Especifica a região para a qual criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="0e507-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="0e507-122">O padrão é o Eastus.</span><span class="sxs-lookup"><span data-stu-id="0e507-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="0e507-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0e507-123">-ResourceName</span></span>
<span data-ttu-id="0e507-124">Especifica o nome do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="0e507-125">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="0e507-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="0e507-126">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="0e507-126">-TenantId</span></span>
<span data-ttu-id="0e507-127">Especifica o Tenantid do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="0e507-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e507-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e507-129">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="0e507-130">Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e507-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="0e507-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="0e507-131">-ArmAccessToken</span></span>
<span data-ttu-id="0e507-132">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="0e507-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="0e507-133">Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="0e507-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="0e507-134">-GraphAccessToken</span></span>
<span data-ttu-id="0e507-135">Especifica o token de acesso do gráfico.</span><span class="sxs-lookup"><span data-stu-id="0e507-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="0e507-136">Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="0e507-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="0e507-137">-AccountId</span></span>
<span data-ttu-id="0e507-138">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="0e507-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="0e507-139">Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e507-140">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="0e507-140">-EnvironmentName</span></span>
<span data-ttu-id="0e507-141">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="0e507-142">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="0e507-142">Default is AzureCloud.</span></span>
<span data-ttu-id="0e507-143">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="0e507-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e507-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="0e507-144">-ComputerName</span></span>
<span data-ttu-id="0e507-145">Especifica o nome do cluster ou um do nó do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e507-146">-Credential</span><span class="sxs-lookup"><span data-stu-id="0e507-146">-Credential</span></span>
<span data-ttu-id="0e507-147">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="0e507-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="0e507-148">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e507-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e507-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e507-149">CommonParameters</span></span>
<span data-ttu-id="0e507-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e507-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e507-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e507-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e507-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e507-152">INPUTS</span></span>

## <span data-ttu-id="0e507-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e507-153">OUTPUTS</span></span>

### <span data-ttu-id="0e507-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="0e507-154">PSCustomObject.</span></span> <span data-ttu-id="0e507-155">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="0e507-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="0e507-156">Resultado: êxito ou falha ou PendingForAdminConsent ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="0e507-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="0e507-157">ResourceId: ID do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="0e507-158">PortalResourceURL: URL de recurso do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e507-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="0e507-159">PortalAADAppPermissionsURL: URL do portal do Azure para a página de permissões do aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="0e507-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="0e507-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e507-160">NOTES</span></span>

## <span data-ttu-id="0e507-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e507-161">RELATED LINKS</span></span>
