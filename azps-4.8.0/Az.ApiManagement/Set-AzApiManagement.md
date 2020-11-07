---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947991"
---
# <span data-ttu-id="2cafc-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="2cafc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cafc-102">SYNOPSIS</span></span>
<span data-ttu-id="2cafc-103">Atualiza um serviço de gerenciamento de API do Azure</span><span class="sxs-lookup"><span data-stu-id="2cafc-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="2cafc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cafc-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cafc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cafc-105">DESCRIPTION</span></span>

<span data-ttu-id="2cafc-106">O cmdlet **set-AzApiManagement** atualiza um serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cafc-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="2cafc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cafc-107">EXAMPLES</span></span>

### <span data-ttu-id="2cafc-108">Exemplo 1: obter um serviço de gerenciamento de API e dimensioná-lo para Premium e adicionar uma região</span><span class="sxs-lookup"><span data-stu-id="2cafc-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="2cafc-109">Este exemplo obtém uma instância de gerenciamento de API, a dimensiona para cinco unidades Premium e, em seguida, adiciona outras três unidades à região Premium.</span><span class="sxs-lookup"><span data-stu-id="2cafc-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="2cafc-110">Exemplo 2: implantação de atualização (VNET externa)</span><span class="sxs-lookup"><span data-stu-id="2cafc-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="2cafc-111">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* externo.</span><span class="sxs-lookup"><span data-stu-id="2cafc-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="2cafc-112">Exemplo 3: criar e inicializar uma instância do PsApiManagementCustomHostNameConfiguration usando um segredo do recurso de keyvault</span><span class="sxs-lookup"><span data-stu-id="2cafc-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
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

### <span data-ttu-id="2cafc-113">Exemplo 4: atualizar emails do Publisher, email NotificationSender e nome da organização</span><span class="sxs-lookup"><span data-stu-id="2cafc-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="2cafc-114">OS</span><span class="sxs-lookup"><span data-stu-id="2cafc-114">PARAMETERS</span></span>

### <span data-ttu-id="2cafc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cafc-115">-AsJob</span></span>
<span data-ttu-id="2cafc-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2cafc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cafc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cafc-117">-DefaultProfile</span></span>
<span data-ttu-id="2cafc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cafc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cafc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cafc-119">-InputObject</span></span>
<span data-ttu-id="2cafc-120">A instância ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2cafc-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="2cafc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cafc-121">-PassThru</span></span>
<span data-ttu-id="2cafc-122">Envia o PsApiManagement atualizado para o pipeline se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2cafc-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="2cafc-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2cafc-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2cafc-124">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cafc-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2cafc-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2cafc-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="2cafc-126">Atribua identidades de usuários a este servidor para uso com os serviços de gerenciamento de chaves, como o keyvault do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cafc-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2cafc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2cafc-127">-Confirm</span></span>
<span data-ttu-id="2cafc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cafc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cafc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cafc-129">-WhatIf</span></span>
<span data-ttu-id="2cafc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cafc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cafc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cafc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cafc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cafc-132">CommonParameters</span></span>
<span data-ttu-id="2cafc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cafc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cafc-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cafc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cafc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cafc-135">INPUTS</span></span>

### <span data-ttu-id="2cafc-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2cafc-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cafc-137">OUTPUTS</span></span>

### <span data-ttu-id="2cafc-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2cafc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cafc-139">NOTES</span></span>

## <span data-ttu-id="2cafc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cafc-140">RELATED LINKS</span></span>

[<span data-ttu-id="2cafc-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="2cafc-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="2cafc-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2cafc-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
