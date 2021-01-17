---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427898"
---
# <span data-ttu-id="19510-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="19510-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="19510-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19510-102">SYNOPSIS</span></span>
<span data-ttu-id="19510-103">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="19510-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19510-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="19510-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19510-105">DESCRIPTION</span></span>
<span data-ttu-id="19510-106">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="19510-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19510-107">EXAMPLES</span></span>

### <span data-ttu-id="19510-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="19510-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="19510-109">\>Registro C:\PS-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" resultado: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL:https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="19510-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="19510-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="19510-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="19510-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-NomeDoComputador ClusterNode1 Result: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="19510-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="19510-112">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="19510-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="19510-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="19510-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="19510-114">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="19510-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="19510-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region oesteus-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="19510-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="19510-116">OS</span><span class="sxs-lookup"><span data-stu-id="19510-116">PARAMETERS</span></span>

### <span data-ttu-id="19510-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="19510-117">-AccountId</span></span>
<span data-ttu-id="19510-118">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="19510-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="19510-119">Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="19510-120">-ArmAccessToken</span></span>
<span data-ttu-id="19510-121">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="19510-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="19510-122">Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="19510-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="19510-123">-CertificateThumbprint</span></span>
<span data-ttu-id="19510-124">Especifica a impressão digital do certificado disponível em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="19510-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="19510-125">O usuário é responsável por gerenciar o certificado.</span><span class="sxs-lookup"><span data-stu-id="19510-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="19510-126">-ComputerName</span></span>
<span data-ttu-id="19510-127">Especifica o nome do cluster ou um do nó do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="19510-128">-Credential</span></span>
<span data-ttu-id="19510-129">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="19510-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="19510-130">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19510-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-131">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="19510-131">-EnvironmentName</span></span>
<span data-ttu-id="19510-132">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="19510-133">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="19510-133">Default is AzureCloud.</span></span>
<span data-ttu-id="19510-134">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="19510-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="19510-135">-GraphAccessToken</span></span>
<span data-ttu-id="19510-136">Especifica o token de acesso do gráfico.</span><span class="sxs-lookup"><span data-stu-id="19510-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="19510-137">Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="19510-138">-Região</span><span class="sxs-lookup"><span data-stu-id="19510-138">-Region</span></span>
<span data-ttu-id="19510-139">Especifica a região para a qual criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="19510-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="19510-140">O padrão é o Eastus.</span><span class="sxs-lookup"><span data-stu-id="19510-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="19510-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="19510-141">-RepairRegistration</span></span>
<span data-ttu-id="19510-142">Reparar o registro do HCI do Azure Stack atual com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="19510-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="19510-143">Esse cmdlet exclui os certificados locais nos nós clusterizados e os certificados remotos no aplicativo Azure AD na nuvem e gera novos certificados de substituição para ambos.</span><span class="sxs-lookup"><span data-stu-id="19510-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="19510-144">O grupo de recursos, o nome do recurso e outras opções de registro são preservados.</span><span class="sxs-lookup"><span data-stu-id="19510-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="19510-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19510-145">-ResourceGroupName</span></span>
<span data-ttu-id="19510-146">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="19510-147">Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19510-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="19510-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19510-148">-ResourceName</span></span>
<span data-ttu-id="19510-149">Especifica o nome do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="19510-150">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="19510-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="19510-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19510-151">-SubscriptionId</span></span>
<span data-ttu-id="19510-152">Especifica a assinatura do Azure para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="19510-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="19510-153">Esse é o único parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="19510-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-154">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="19510-154">-TenantId</span></span>
<span data-ttu-id="19510-155">Especifica o Tenantid do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="19510-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="19510-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="19510-157">Use a autenticação de código do dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="19510-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="19510-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19510-158">CommonParameters</span></span>
<span data-ttu-id="19510-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19510-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19510-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19510-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19510-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19510-161">INPUTS</span></span>

## <span data-ttu-id="19510-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19510-162">OUTPUTS</span></span>

### <span data-ttu-id="19510-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="19510-163">PSCustomObject.</span></span> <span data-ttu-id="19510-164">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="19510-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="19510-165">Resultado: êxito ou falha ou PendingForAdminConsent ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="19510-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="19510-166">ResourceId: ID do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="19510-167">PortalResourceURL: URL de recurso do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="19510-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="19510-168">PortalAADAppPermissionsURL: URL do portal do Azure para a página de permissões do aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="19510-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="19510-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19510-169">NOTES</span></span>

## <span data-ttu-id="19510-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19510-170">RELATED LINKS</span></span>
