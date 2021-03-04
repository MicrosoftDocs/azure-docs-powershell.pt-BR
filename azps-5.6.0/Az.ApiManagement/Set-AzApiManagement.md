---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: 3f1ab16dd6bf8dd264bdb4e4427d45197feace7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887833"
---
# <span data-ttu-id="c331e-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="c331e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c331e-102">SYNOPSIS</span></span>
<span data-ttu-id="c331e-103">Atualiza um serviço de Gerenciamento de Api do Azure</span><span class="sxs-lookup"><span data-stu-id="c331e-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="c331e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c331e-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c331e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c331e-105">DESCRIPTION</span></span>

<span data-ttu-id="c331e-106">O cmdlet **Set-AzApiManagement** atualiza um serviço de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="c331e-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="c331e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c331e-107">EXAMPLES</span></span>

### <span data-ttu-id="c331e-108">Exemplo 1: Obter um serviço de Gerenciamento de API e dimensioná-lo para Premium e Adicionar uma região</span><span class="sxs-lookup"><span data-stu-id="c331e-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="c331e-109">Este exemplo obtém uma instância de Gerenciamento de Api, dimensiona-a para cinco unidades premium e adiciona mais três unidades à região premium.</span><span class="sxs-lookup"><span data-stu-id="c331e-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="c331e-110">Exemplo 2: Implantação de atualização (VNET externa)</span><span class="sxs-lookup"><span data-stu-id="c331e-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="c331e-111">Este comando atualiza uma implantação existente de Gerenciamento de API e ins junta-se a um *VpnType externo.*</span><span class="sxs-lookup"><span data-stu-id="c331e-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="c331e-112">Exemplo 3: Criar e inicializar uma instância de PsApiManagementCustomHostNameConfiguration usando um Segredo do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="c331e-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="c331e-113">Exemplo 4: Atualizar Email do Publisher, NotificationSender Email e Nome da Organização</span><span class="sxs-lookup"><span data-stu-id="c331e-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="c331e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c331e-114">PARAMETERS</span></span>

### <span data-ttu-id="c331e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c331e-115">-AsJob</span></span>
<span data-ttu-id="c331e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c331e-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c331e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c331e-117">-DefaultProfile</span></span>
<span data-ttu-id="c331e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c331e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c331e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c331e-119">-InputObject</span></span>
<span data-ttu-id="c331e-120">A instância ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c331e-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c331e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c331e-121">-PassThru</span></span>
<span data-ttu-id="c331e-122">Envia PsApiManagement atualizado para pipeline se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c331e-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c331e-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c331e-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c331e-124">Gere e atribua uma Identidade do Active Directory do Azure para esse servidor para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c331e-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c331e-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c331e-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="c331e-126">Atribua identidades de usuário a esse servidor para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c331e-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c331e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c331e-127">-Confirm</span></span>
<span data-ttu-id="c331e-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c331e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c331e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c331e-129">-WhatIf</span></span>
<span data-ttu-id="c331e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c331e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c331e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c331e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c331e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c331e-132">CommonParameters</span></span>
<span data-ttu-id="c331e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c331e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c331e-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c331e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c331e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c331e-135">INPUTS</span></span>

### <span data-ttu-id="c331e-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c331e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c331e-137">OUTPUTS</span></span>

### <span data-ttu-id="c331e-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c331e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="c331e-139">NOTES</span></span>

## <span data-ttu-id="c331e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c331e-140">RELATED LINKS</span></span>

[<span data-ttu-id="c331e-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c331e-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c331e-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c331e-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
