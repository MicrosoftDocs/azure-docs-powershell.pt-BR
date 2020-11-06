---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428637"
---
# <span data-ttu-id="55710-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="55710-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="55710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55710-102">SYNOPSIS</span></span>
<span data-ttu-id="55710-103">Define uma configuração de nome de host personalizada para um proxy ou um portal do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="55710-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55710-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55710-104">SYNTAX</span></span>

### <span data-ttu-id="55710-105">SetSpecificService (padrão)</span><span class="sxs-lookup"><span data-stu-id="55710-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55710-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="55710-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55710-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55710-107">DESCRIPTION</span></span>
<span data-ttu-id="55710-108">O cmdlet **set-AzureRmApiManagementHostnames** aplica uma configuração de nome de host personalizada a um proxy ou portal do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="55710-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="55710-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55710-109">EXAMPLES</span></span>

### <span data-ttu-id="55710-110">Exemplo 1: definir a configuração do nome do host personalizado para um proxy e um portal</span><span class="sxs-lookup"><span data-stu-id="55710-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="55710-111">Este comando define a configuração do nome do host personalizado para o proxy e o Portal.</span><span class="sxs-lookup"><span data-stu-id="55710-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="55710-112">Exemplo 2: configurar um nome de host personalizado para um proxy e um portal</span><span class="sxs-lookup"><span data-stu-id="55710-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="55710-113">Este exemplo configura um nome de host personalizado para proxy e Portal.</span><span class="sxs-lookup"><span data-stu-id="55710-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="55710-114">Você precisa importar certificados correspondentes e, em seguida, aplicar os nomes de hosts personalizados.</span><span class="sxs-lookup"><span data-stu-id="55710-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="55710-115">OS</span><span class="sxs-lookup"><span data-stu-id="55710-115">PARAMETERS</span></span>

### <span data-ttu-id="55710-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="55710-116">-ApiManagement</span></span>
<span data-ttu-id="55710-117">Especifica a instância **PsApiManagement** para a qual esse cmdlet obtém os parâmetros *PortalHostnameConfiguration* e *ProxyHostnameConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="55710-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55710-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55710-118">-DefaultProfile</span></span>
<span data-ttu-id="55710-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55710-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55710-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="55710-120">-Name</span></span>
<span data-ttu-id="55710-121">Especifica o nome da instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="55710-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55710-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55710-122">-PassThru</span></span>
<span data-ttu-id="55710-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="55710-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55710-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="55710-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55710-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="55710-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="55710-126">Especifica a configuração do nome do host do portal personalizado.</span><span class="sxs-lookup"><span data-stu-id="55710-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="55710-127">Passar $null para o cmdlet define o nome do host padrão.</span><span class="sxs-lookup"><span data-stu-id="55710-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55710-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="55710-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="55710-129">Especifica a configuração do nome do host de proxy personalizado.</span><span class="sxs-lookup"><span data-stu-id="55710-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="55710-130">Passar $null define o nome do host padrão.</span><span class="sxs-lookup"><span data-stu-id="55710-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55710-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55710-131">-ResourceGroupName</span></span>
<span data-ttu-id="55710-132">Especifica o nome do grupo de recursos sob o qual existe a instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="55710-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55710-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55710-133">CommonParameters</span></span>
<span data-ttu-id="55710-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55710-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55710-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55710-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55710-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55710-136">INPUTS</span></span>

### <span data-ttu-id="55710-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="55710-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="55710-138">Parâmetros: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55710-138">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="55710-139">System. String</span><span class="sxs-lookup"><span data-stu-id="55710-139">System.String</span></span>

### <span data-ttu-id="55710-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="55710-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="55710-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55710-141">OUTPUTS</span></span>

### <span data-ttu-id="55710-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="55710-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="55710-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55710-143">NOTES</span></span>

## <span data-ttu-id="55710-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55710-144">RELATED LINKS</span></span>

[<span data-ttu-id="55710-145">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="55710-145">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="55710-146">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="55710-146">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

