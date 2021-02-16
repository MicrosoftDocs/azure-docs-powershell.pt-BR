---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 552a6a317524de6d0f1db86a9a69a2733826d3f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113415"
---
# <span data-ttu-id="25686-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="25686-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="25686-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25686-102">SYNOPSIS</span></span>
<span data-ttu-id="25686-103">Atualiza uma configuração vpnserverconfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="25686-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="25686-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25686-104">SYNTAX</span></span>

### <span data-ttu-id="25686-105">ByVpnServerConfigurationName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25686-105">ByVpnServerConfigurationName (Default)</span></span>
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

### <span data-ttu-id="25686-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="25686-106">ByVpnServerConfigurationObject</span></span>
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

### <span data-ttu-id="25686-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="25686-107">ByVpnServerConfigurationResourceId</span></span>
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

## <span data-ttu-id="25686-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="25686-108">DESCRIPTION</span></span>
<span data-ttu-id="25686-109">O cmdlet **Update-AzVpnServerConfiguration** permite que você atualize o vpnServerConfiguration existente com diferentes VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e para definir parâmetros relacionados ao tipo de autenticação de vpn selecionado, de acordo com o requisito do cliente para a conectividade do Ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="25686-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="25686-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25686-110">EXAMPLES</span></span>

### <span data-ttu-id="25686-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25686-111">Example 1</span></span>
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

<span data-ttu-id="25686-112">O comando acima atualizará uma Configuração VpnServerConfiguration existente com VpnProtocol como IkeV2.</span><span class="sxs-lookup"><span data-stu-id="25686-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="25686-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25686-113">PARAMETERS</span></span>

### <span data-ttu-id="25686-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="25686-114">-AadAudience</span></span>
<span data-ttu-id="25686-115">Audiência do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="25686-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="25686-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="25686-116">-AadIssuer</span></span>
<span data-ttu-id="25686-117">Emissor do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="25686-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="25686-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="25686-118">-AadTenant</span></span>
<span data-ttu-id="25686-119">Locatário do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="25686-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="25686-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25686-120">-AsJob</span></span>
<span data-ttu-id="25686-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="25686-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25686-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25686-122">-DefaultProfile</span></span>
<span data-ttu-id="25686-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25686-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25686-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25686-124">-InputObject</span></span>
<span data-ttu-id="25686-125">O objeto de configuração do servidor vpn a ser modificado</span><span class="sxs-lookup"><span data-stu-id="25686-125">The vpn server configuration object to be modified</span></span>

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

### <span data-ttu-id="25686-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="25686-126">-Name</span></span>
<span data-ttu-id="25686-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="25686-127">The resource name.</span></span>

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

### <span data-ttu-id="25686-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="25686-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="25686-129">Uma lista dos caminhos dos arquivos de RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="25686-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="25686-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="25686-130">-RadiusServerAddress</span></span>
<span data-ttu-id="25686-131">Endereço do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="25686-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="25686-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="25686-132">-RadiusServerList</span></span>
<span data-ttu-id="25686-133">P2S Servidores externos de múltiplos raios.</span><span class="sxs-lookup"><span data-stu-id="25686-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="25686-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="25686-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="25686-135">Uma lista dos caminhos dos arquivos de RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="25686-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="25686-136">-RadiusServerSecsec</span><span class="sxs-lookup"><span data-stu-id="25686-136">-RadiusServerSecret</span></span>
<span data-ttu-id="25686-137">Segredo do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="25686-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="25686-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25686-138">-ResourceGroupName</span></span>
<span data-ttu-id="25686-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25686-139">The resource group name.</span></span>

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

### <span data-ttu-id="25686-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25686-140">-ResourceId</span></span>
<span data-ttu-id="25686-141">A ID de recurso do Azure para a configuração do servidor vpn.</span><span class="sxs-lookup"><span data-stu-id="25686-141">The Azure resource ID for the vpn server configuration.</span></span>

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

### <span data-ttu-id="25686-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="25686-142">-Tag</span></span>
<span data-ttu-id="25686-143">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="25686-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="25686-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="25686-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="25686-145">A lista de protocolos de túnel do cliente P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="25686-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="25686-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="25686-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="25686-147">Uma lista de políticas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="25686-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="25686-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="25686-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="25686-149">Uma lista de VpnClientCertificates a serem revogados caminhos de arquivos</span><span class="sxs-lookup"><span data-stu-id="25686-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="25686-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="25686-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="25686-151">Uma lista de VpnClientRootCertificates para adicionar os caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="25686-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="25686-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="25686-152">-VpnProtocol</span></span>
<span data-ttu-id="25686-153">A lista de protocolos de túnel do cliente P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="25686-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="25686-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="25686-154">-Confirm</span></span>
<span data-ttu-id="25686-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25686-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25686-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25686-156">-WhatIf</span></span>
<span data-ttu-id="25686-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="25686-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25686-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25686-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25686-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25686-159">CommonParameters</span></span>
<span data-ttu-id="25686-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25686-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25686-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25686-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25686-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="25686-162">INPUTS</span></span>

### <span data-ttu-id="25686-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="25686-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="25686-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="25686-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="25686-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="25686-165">OUTPUTS</span></span>

### <span data-ttu-id="25686-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="25686-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="25686-167">Notas</span><span class="sxs-lookup"><span data-stu-id="25686-167">NOTES</span></span>

## <span data-ttu-id="25686-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25686-168">RELATED LINKS</span></span>
