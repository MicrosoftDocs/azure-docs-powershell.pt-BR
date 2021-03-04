---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: 2a6e94512e8bc9bed980c76b5430118d74bd3f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889882"
---
# <span data-ttu-id="ab5b6-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="ab5b6-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="ab5b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5b6-103">Register-AzStackHCI cria um recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="ab5b6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ab5b6-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="ab5b6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ab5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ab5b6-106">Register-AzStackHCI cria um recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="ab5b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-107">EXAMPLES</span></span>

### <span data-ttu-id="ab5b6-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ab5b6-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="ab5b6-109">Invocando um dos nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="ab5b6-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="ab5b6-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ab5b6-111">Invocando do nó de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-111">Invoking from the management node.</span></span>

### <span data-ttu-id="ab5b6-112">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="ab5b6-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ab5b6-113">Invocando do WAC.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-113">Invoking from WAC.</span></span>

### <span data-ttu-id="ab5b6-114">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="ab5b6-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ab5b6-115">Invocando com todos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="ab5b6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-116">PARAMETERS</span></span>

### <span data-ttu-id="ab5b6-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ab5b6-117">-AccountId</span></span>
<span data-ttu-id="ab5b6-118">Especifica o token de ARM de acesso.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="ab5b6-119">Especificar isso junto com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="ab5b6-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="ab5b6-120">-ArmAccessToken</span></span>
<span data-ttu-id="ab5b6-121">Especifica o token de ARM de acesso.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="ab5b6-122">Especificar isso junto com GraphAccessToken e AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="ab5b6-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ab5b6-123">-CertificateThumbprint</span></span>
<span data-ttu-id="ab5b6-124">Especifica a impressão digital do certificado disponível em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="ab5b6-125">O usuário é responsável pelo gerenciamento do certificado.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="ab5b6-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ab5b6-126">-ComputerName</span></span>
<span data-ttu-id="ab5b6-127">Especifica o nome do cluster ou um dos nós de cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="ab5b6-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="ab5b6-128">-Credential</span></span>
<span data-ttu-id="ab5b6-129">Especifica a credencial do ComputerName.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ab5b6-130">O padrão é o usuário atual executando o Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="ab5b6-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ab5b6-131">-EnvironmentName</span></span>
<span data-ttu-id="ab5b6-132">Especifica o Ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ab5b6-133">O padrão é o AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-133">Default is AzureCloud.</span></span>
<span data-ttu-id="ab5b6-134">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ab5b6-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="ab5b6-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ab5b6-135">-GraphAccessToken</span></span>
<span data-ttu-id="ab5b6-136">Especifica o token de acesso graph.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="ab5b6-137">Especificar isso junto com ArmAccessToken e AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="ab5b6-138">-Region</span><span class="sxs-lookup"><span data-stu-id="ab5b6-138">-Region</span></span>
<span data-ttu-id="ab5b6-139">Especifica a região para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="ab5b6-140">O padrão é EastUS.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="ab5b6-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="ab5b6-141">-RepairRegistration</span></span>
<span data-ttu-id="ab5b6-142">Repare o registro atual do Azure Stack HCI com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="ab5b6-143">Este cmdlet exclui os certificados locais nos nós agrupados e os certificados remotos no aplicativo do Azure AD na nuvem e gera novos certificados de substituição para ambos.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="ab5b6-144">O grupo de recursos, o nome do recurso e outras opções de registro são preservados.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="ab5b6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5b6-145">-ResourceGroupName</span></span>
<span data-ttu-id="ab5b6-146">Especifica o nome do Grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="ab5b6-147">Se não especificado \<LocalClusterName\> -rg será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="ab5b6-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ab5b6-148">-ResourceName</span></span>
<span data-ttu-id="ab5b6-149">Especifica o nome do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="ab5b6-150">Se não for especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="ab5b6-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab5b6-151">-SubscriptionId</span></span>
<span data-ttu-id="ab5b6-152">Especifica a Assinatura do Azure para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="ab5b6-153">Esse é o único parâmetro Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="ab5b6-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ab5b6-154">-TenantId</span></span>
<span data-ttu-id="ab5b6-155">Especifica o TenantId do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="ab5b6-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ab5b6-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="ab5b6-157">Use a autenticação de código de dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="ab5b6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5b6-158">CommonParameters</span></span>
<span data-ttu-id="ab5b6-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5b6-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab5b6-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5b6-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-161">INPUTS</span></span>

## <span data-ttu-id="ab5b6-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-162">OUTPUTS</span></span>

### <span data-ttu-id="ab5b6-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-163">PSCustomObject.</span></span> <span data-ttu-id="ab5b6-164">Retorna propriedades a seguir em PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="ab5b6-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ab5b6-165">Resultado: Êxito ou Falha ou PendingForAdminConsent ou Cancelado.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="ab5b6-166">ResourceId: ID do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="ab5b6-167">PortalResourceURL: URL do Recurso do Portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="ab5b6-168">PortalAADAppPermissionsURL: página URL do Portal do Azure para permissões do aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="ab5b6-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="ab5b6-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="ab5b6-169">NOTES</span></span>

## <span data-ttu-id="ab5b6-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab5b6-170">RELATED LINKS</span></span>
