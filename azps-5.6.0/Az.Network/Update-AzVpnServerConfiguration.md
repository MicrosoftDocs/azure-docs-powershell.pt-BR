---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885316"
---
# <span data-ttu-id="b7924-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7924-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b7924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7924-102">SYNOPSIS</span></span>
<span data-ttu-id="b7924-103">Atualiza um VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="b7924-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="b7924-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7924-104">SYNTAX</span></span>

### <span data-ttu-id="b7924-105">ByVpnServerConfigurationName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7924-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7924-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b7924-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7924-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b7924-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7924-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7924-108">DESCRIPTION</span></span>
<span data-ttu-id="b7924-109">O cmdlet **Update-AzVpnServerConfiguration** permite que você atualize o VpnServerConfiguration existente com vpnProtocols diferentes, VpnAuthenticationTypes, IpsecPolicies e definir parâmetros relacionados ao tipo de autenticação vpn selecionado de acordo com o requisito do cliente para conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="b7924-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="b7924-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7924-110">EXAMPLES</span></span>

### <span data-ttu-id="b7924-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7924-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="b7924-112">O comando acima atualizará um VpnServerConfiguration existente com VpnProtocol como IkeV2.</span><span class="sxs-lookup"><span data-stu-id="b7924-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="b7924-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7924-113">PARAMETERS</span></span>

### <span data-ttu-id="b7924-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="b7924-114">-AadAudience</span></span>
<span data-ttu-id="b7924-115">Audiência do AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="b7924-116">-AadIssuer</span></span>
<span data-ttu-id="b7924-117">Emissor AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="b7924-118">-AadTenant</span></span>
<span data-ttu-id="b7924-119">Locatário AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7924-120">-AsJob</span></span>
<span data-ttu-id="b7924-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b7924-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7924-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7924-122">-DefaultProfile</span></span>
<span data-ttu-id="b7924-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7924-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7924-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7924-124">-InputObject</span></span>
<span data-ttu-id="b7924-125">O objeto de configuração do servidor vpn a ser modificado</span><span class="sxs-lookup"><span data-stu-id="b7924-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b7924-126">-Name</span></span>
<span data-ttu-id="b7924-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b7924-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7924-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="b7924-129">Uma lista de caminhos dos arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7924-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b7924-130">-RadiusServerAddress</span></span>
<span data-ttu-id="b7924-131">Endereço do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-131">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="b7924-132">-RadiusServerList</span></span>
<span data-ttu-id="b7924-133">Servidores de vários raios externos P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7924-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="b7924-135">Uma lista de caminhos dos arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7924-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b7924-136">-RadiusServerSecret</span></span>
<span data-ttu-id="b7924-137">Segredo do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7924-138">-ResourceGroupName</span></span>
<span data-ttu-id="b7924-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7924-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7924-140">-ResourceId</span></span>
<span data-ttu-id="b7924-141">A ID de recurso do Azure para a configuração do servidor vpn.</span><span class="sxs-lookup"><span data-stu-id="b7924-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7924-142">-Tag</span></span>
<span data-ttu-id="b7924-143">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b7924-143">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b7924-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="b7924-145">A lista de protocolos de túnel de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-145">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b7924-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b7924-147">Uma lista de políticas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7924-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7924-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="b7924-149">Uma lista de VpnClientCertificates a serem revogados caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="b7924-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b7924-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="b7924-151">Uma lista de VpnClientRootCertificates a serem adicionados caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="b7924-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="b7924-152">-VpnProtocol</span></span>
<span data-ttu-id="b7924-153">A lista de protocolos de túnel de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="b7924-153">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7924-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7924-154">-Confirm</span></span>
<span data-ttu-id="b7924-155">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7924-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7924-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7924-156">-WhatIf</span></span>
<span data-ttu-id="b7924-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7924-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7924-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7924-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7924-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7924-159">CommonParameters</span></span>
<span data-ttu-id="b7924-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7924-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7924-161">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7924-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7924-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7924-162">INPUTS</span></span>

### <span data-ttu-id="b7924-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7924-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="b7924-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b7924-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="b7924-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7924-165">OUTPUTS</span></span>

### <span data-ttu-id="b7924-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7924-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b7924-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7924-167">NOTES</span></span>

## <span data-ttu-id="b7924-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7924-168">RELATED LINKS</span></span>
