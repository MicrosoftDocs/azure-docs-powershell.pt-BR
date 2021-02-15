---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: a96ca28b750628eef1b0395e5867bb7f7341fba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112519"
---
# <span data-ttu-id="002fb-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="002fb-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="002fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="002fb-102">SYNOPSIS</span></span>
<span data-ttu-id="002fb-103">Register-AzStackHCI cria um recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="002fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="002fb-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="002fb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="002fb-105">DESCRIPTION</span></span>
<span data-ttu-id="002fb-106">Register-AzStackHCI cria um recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e registra o cluster local com o Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="002fb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="002fb-107">EXAMPLES</span></span>

### <span data-ttu-id="002fb-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="002fb-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="002fb-109">Invoking on a of the cluster node.</span><span class="sxs-lookup"><span data-stu-id="002fb-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="002fb-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="002fb-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="002fb-111">Revogando do nó de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="002fb-111">Invoking from the management node.</span></span>

### <span data-ttu-id="002fb-112">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="002fb-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="002fb-113">Invoking from WAC.</span><span class="sxs-lookup"><span data-stu-id="002fb-113">Invoking from WAC.</span></span>

### <span data-ttu-id="002fb-114">EXEMPLO 4</span><span class="sxs-lookup"><span data-stu-id="002fb-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="002fb-115">Revogar com todos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="002fb-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="002fb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="002fb-116">PARAMETERS</span></span>

### <span data-ttu-id="002fb-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="002fb-117">-AccountId</span></span>
<span data-ttu-id="002fb-118">Especifica o token de acesso ARM.</span><span class="sxs-lookup"><span data-stu-id="002fb-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="002fb-119">Especificar isso junto com o ArmAccessToken e o GraphAccessToken evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="002fb-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="002fb-120">-ArmAccessToken</span></span>
<span data-ttu-id="002fb-121">Especifica o token de acesso ARM.</span><span class="sxs-lookup"><span data-stu-id="002fb-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="002fb-122">Especificar isso junto com o GraphAccessToken e o AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="002fb-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="002fb-123">-CertificateThumbprint</span></span>
<span data-ttu-id="002fb-124">Especifica a impressão digital do certificado disponível em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="002fb-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="002fb-125">O usuário é responsável pelo gerenciamento do certificado.</span><span class="sxs-lookup"><span data-stu-id="002fb-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="002fb-126">-NomedoCompr computador</span><span class="sxs-lookup"><span data-stu-id="002fb-126">-ComputerName</span></span>
<span data-ttu-id="002fb-127">Especifica o nome do cluster ou um do nó de cluster no cluster local que está sendo registrado no Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="002fb-128">-Credencial</span><span class="sxs-lookup"><span data-stu-id="002fb-128">-Credential</span></span>
<span data-ttu-id="002fb-129">Especifica a credencial para o NomeDoCompt.</span><span class="sxs-lookup"><span data-stu-id="002fb-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="002fb-130">O padrão é o usuário atual executando o Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="002fb-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="002fb-131">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="002fb-131">-EnvironmentName</span></span>
<span data-ttu-id="002fb-132">Especifica o Ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="002fb-133">O padrão é o AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="002fb-133">Default is AzureCloud.</span></span>
<span data-ttu-id="002fb-134">Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSCloudment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="002fb-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="002fb-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="002fb-135">-GraphAccessToken</span></span>
<span data-ttu-id="002fb-136">Especifica o token de acesso Graph.</span><span class="sxs-lookup"><span data-stu-id="002fb-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="002fb-137">Especificar isso junto com ArmAccessToken e AccountId evitará o logon interativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="002fb-138">-Região</span><span class="sxs-lookup"><span data-stu-id="002fb-138">-Region</span></span>
<span data-ttu-id="002fb-139">Especifica a Região para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="002fb-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="002fb-140">O padrão é o EastUS.</span><span class="sxs-lookup"><span data-stu-id="002fb-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="002fb-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="002fb-141">-RepairRegistration</span></span>
<span data-ttu-id="002fb-142">Repare o registro atual do HCI do Azure Stack com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="002fb-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="002fb-143">Este cmdlet exclui os certificados locais nos nós clusterados e os certificados remotos no aplicativo Azure AD na nuvem e gera novos certificados de substituição para ambos.</span><span class="sxs-lookup"><span data-stu-id="002fb-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="002fb-144">O grupo de recursos, o nome do recurso e outras opções de registro são preservados.</span><span class="sxs-lookup"><span data-stu-id="002fb-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="002fb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002fb-145">-ResourceGroupName</span></span>
<span data-ttu-id="002fb-146">Especifica o nome do Grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="002fb-147">Se não especificado \<LocalClusterName\> , -rg será usado como nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="002fb-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="002fb-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="002fb-148">-ResourceName</span></span>
<span data-ttu-id="002fb-149">Especifica o nome do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="002fb-150">Se não especificado, o nome do cluster local será usado.</span><span class="sxs-lookup"><span data-stu-id="002fb-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="002fb-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="002fb-151">-SubscriptionId</span></span>
<span data-ttu-id="002fb-152">Especifica a Assinatura do Azure para criar o recurso.</span><span class="sxs-lookup"><span data-stu-id="002fb-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="002fb-153">Este é o único parâmetro Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="002fb-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="002fb-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="002fb-154">-TenantId</span></span>
<span data-ttu-id="002fb-155">Especifica o Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="002fb-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="002fb-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="002fb-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="002fb-157">Use a autenticação de código do dispositivo em vez de um prompt interativo do navegador.</span><span class="sxs-lookup"><span data-stu-id="002fb-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="002fb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002fb-158">CommonParameters</span></span>
<span data-ttu-id="002fb-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002fb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002fb-160">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="002fb-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002fb-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="002fb-161">INPUTS</span></span>

## <span data-ttu-id="002fb-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="002fb-162">OUTPUTS</span></span>

### <span data-ttu-id="002fb-163">Pscustomobject.</span><span class="sxs-lookup"><span data-stu-id="002fb-163">PSCustomObject.</span></span> <span data-ttu-id="002fb-164">Retorna propriedades a seguir no PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="002fb-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="002fb-165">Resultado: Êxito ou Falha ou PendenteForAdminConsent ou Cancelado.</span><span class="sxs-lookup"><span data-stu-id="002fb-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="002fb-166">ResourceId: ID do recurso criado no Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="002fb-167">PortalResourceURL: URL do Recurso do Portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="002fb-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="002fb-168">PortalAADAppPermissionsURL: URL do Portal do Azure para a página de permissões do aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="002fb-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="002fb-169">Notas</span><span class="sxs-lookup"><span data-stu-id="002fb-169">NOTES</span></span>

## <span data-ttu-id="002fb-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="002fb-170">RELATED LINKS</span></span>
