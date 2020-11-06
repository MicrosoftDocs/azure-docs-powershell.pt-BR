---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609441"
---
# <span data-ttu-id="3ae8b-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="3ae8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ae8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae8b-103">Atualiza um serviço de gerenciamento de API do Azure</span><span class="sxs-lookup"><span data-stu-id="3ae8b-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ae8b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ae8b-105">DESCRIPTION</span></span>

<span data-ttu-id="3ae8b-106">O cmdlet **set-AzureRmApiManagement** atualiza um serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="3ae8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ae8b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae8b-108">Exemplo 1 obter um serviço de gerenciamento de API e dimensioná-lo para Premium e adicionar uma região</span><span class="sxs-lookup"><span data-stu-id="3ae8b-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="3ae8b-109">Este exemplo obtém uma instância de gerenciamento de API, a dimensiona para cinco unidades Premium e, em seguida, adiciona outras três unidades à região Premium.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="3ae8b-110">Exemplo 2: implantação de atualização (VNET externa)</span><span class="sxs-lookup"><span data-stu-id="3ae8b-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="3ae8b-111">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* externo.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="3ae8b-112">Exemplo 3: criar e inicializar uma instância do PsApiManagementCustomHostNameConfiguration usando um segredo do recurso de keyvault</span><span class="sxs-lookup"><span data-stu-id="3ae8b-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="3ae8b-113">OS</span><span class="sxs-lookup"><span data-stu-id="3ae8b-113">PARAMETERS</span></span>

### <span data-ttu-id="3ae8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ae8b-114">-AsJob</span></span>
<span data-ttu-id="3ae8b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3ae8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ae8b-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3ae8b-116">-AssignIdentity</span></span>
<span data-ttu-id="3ae8b-117">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3ae8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae8b-118">-DefaultProfile</span></span>
<span data-ttu-id="3ae8b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae8b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ae8b-120">-InputObject</span></span>
<span data-ttu-id="3ae8b-121">A instância ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="3ae8b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ae8b-122">-PassThru</span></span>
<span data-ttu-id="3ae8b-123">Envia o PsApiManagement atualizado para o pipeline se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="3ae8b-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ae8b-124">-Confirm</span></span>
<span data-ttu-id="3ae8b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae8b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae8b-126">-WhatIf</span></span>
<span data-ttu-id="3ae8b-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ae8b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae8b-129">CommonParameters</span></span>
<span data-ttu-id="3ae8b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae8b-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae8b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae8b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ae8b-132">INPUTS</span></span>

### <span data-ttu-id="3ae8b-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="3ae8b-134">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ae8b-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3ae8b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ae8b-135">OUTPUTS</span></span>

### <span data-ttu-id="3ae8b-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3ae8b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ae8b-137">NOTES</span></span>

## <span data-ttu-id="3ae8b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ae8b-138">RELATED LINKS</span></span>

[<span data-ttu-id="3ae8b-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="3ae8b-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3ae8b-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ae8b-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
