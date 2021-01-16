---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261034"
---
# <span data-ttu-id="17caa-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="17caa-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="17caa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17caa-102">SYNOPSIS</span></span>
<span data-ttu-id="17caa-103">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="17caa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17caa-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="17caa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17caa-105">DESCRIPTION</span></span>
<span data-ttu-id="17caa-106">Register-AzStackHCI cria um recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="17caa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17caa-107">EXAMPLES</span></span>

### <span data-ttu-id="17caa-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="17caa-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="17caa-109">\>Registro C:\PS-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" resultado: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL:https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="17caa-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="17caa-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="17caa-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="17caa-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-NomeDoComputador ClusterNode1 Result: êxito do ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="17caa-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="17caa-112">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="17caa-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="17caa-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="17caa-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="17caa-114">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="17caa-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="17caa-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region oesteus-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="17caa-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="17caa-116">OS</span><span class="sxs-lookup"><span data-stu-id="17caa-116">PARAMETERS</span></span>

### <span data-ttu-id="17caa-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="17caa-117">-AccountId</span></span>
<span data-ttu-id="17caa-118">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="17caa-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="17caa-119">Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="17caa-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="17caa-120">-ArmAccessToken</span></span>
<span data-ttu-id="17caa-121">Especifica o token de acesso do ARM.</span><span class="sxs-lookup"><span data-stu-id="17caa-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="17caa-122">Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="17caa-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="17caa-123">-CertificateThumbprint</span></span>
<span data-ttu-id="17caa-124">Especifica a impressão digital do certificado disponível em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="17caa-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="17caa-125">O usuário é responsável por gerenciar o certificado.</span><span class="sxs-lookup"><span data-stu-id="17caa-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="17caa-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="17caa-126">-ComputerName</span></span>
<span data-ttu-id="17caa-127">Especifica o nome do cluster ou um do nó do cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="17caa-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="17caa-128">-Credential</span></span>
<span data-ttu-id="17caa-129">Especifica a credencial para o ComputerName.</span><span class="sxs-lookup"><span data-stu-id="17caa-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="17caa-130">Padrão é o usuário atual que está executando o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17caa-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="17caa-131">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="17caa-131">-EnvironmentName</span></span>
<span data-ttu-id="17caa-132">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="17caa-133">O padrão é AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="17caa-133">Default is AzureCloud.</span></span>
<span data-ttu-id="17caa-134">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="17caa-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="17caa-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="17caa-135">-GraphAccessToken</span></span>
<span data-ttu-id="17caa-136">Especifica o token de acesso do gráfico.</span><span class="sxs-lookup"><span data-stu-id="17caa-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="17caa-137">Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="17caa-138">-Região</span><span class="sxs-lookup"><span data-stu-id="17caa-138">-Region</span></span>
<span data-ttu-id="17caa-139">Especifica a região para a qual criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="17caa-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="17caa-140">O padrão é o Eastus.</span><span class="sxs-lookup"><span data-stu-id="17caa-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="17caa-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="17caa-141">-RepairRegistration</span></span>
<span data-ttu-id="17caa-142">Reparar o registro do HCI do Azure Stack atual com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="17caa-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="17caa-143">Esse cmdlet exclui os certificados locais nos nós clusterizados e os certificados remotos no aplicativo Azure AD na nuvem e gera novos certificados de substituição para ambos.</span><span class="sxs-lookup"><span data-stu-id="17caa-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="17caa-144">O grupo de recursos, o nome do recurso e outras opções de registro são preservados.</span><span class="sxs-lookup"><span data-stu-id="17caa-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="17caa-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17caa-145">-ResourceGroupName</span></span>
<span data-ttu-id="17caa-146">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="17caa-147">Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17caa-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="17caa-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="17caa-148">-ResourceName</span></span>
<span data-ttu-id="17caa-149">Especifica o nome do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="17caa-150">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="17caa-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="17caa-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17caa-151">-SubscriptionId</span></span>
<span data-ttu-id="17caa-152">Especifica a assinatura do Azure para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="17caa-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="17caa-153">Esse é o único parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="17caa-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="17caa-154">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="17caa-154">-TenantId</span></span>
<span data-ttu-id="17caa-155">Especifica o Tenantid do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="17caa-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="17caa-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="17caa-157">Use a autenticação de código do dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="17caa-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="17caa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17caa-158">CommonParameters</span></span>
<span data-ttu-id="17caa-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17caa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17caa-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17caa-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17caa-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17caa-161">INPUTS</span></span>

## <span data-ttu-id="17caa-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17caa-162">OUTPUTS</span></span>

### <span data-ttu-id="17caa-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="17caa-163">PSCustomObject.</span></span> <span data-ttu-id="17caa-164">Retorna as propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="17caa-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="17caa-165">Resultado: êxito ou falha ou PendingForAdminConsent ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="17caa-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="17caa-166">ResourceId: ID do recurso do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="17caa-167">PortalResourceURL: URL de recurso do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="17caa-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="17caa-168">PortalAADAppPermissionsURL: URL do portal do Azure para a página de permissões do aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="17caa-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="17caa-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17caa-169">NOTES</span></span>

## <span data-ttu-id="17caa-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17caa-170">RELATED LINKS</span></span>
