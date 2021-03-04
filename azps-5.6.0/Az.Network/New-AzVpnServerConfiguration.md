---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: f093a9f3a30ce1e46c08790d355689fdd9399c79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889430"
---
# <span data-ttu-id="c09b2-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c09b2-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c09b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c09b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c09b2-103">Crie um novo VpnServerConfiguration para a conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="c09b2-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c09b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c09b2-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c09b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c09b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c09b2-106">O cmdlet **New-AzVpnServerConfiguration** permite que você crie um novo VpnServerConfiguration com vpnProtocols diferentes, VpnAuthenticationTypes, IpsecPolicies e definir parâmetros relacionados ao tipo de autenticação vpn selecionado de acordo com o requisito do cliente para conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="c09b2-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="c09b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c09b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c09b2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c09b2-108">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="c09b2-109">O comando acima criará um novo VpnServerConfiguration com VpnAuthenticationType como Certificado.</span><span class="sxs-lookup"><span data-stu-id="c09b2-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="c09b2-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c09b2-110">Example 2</span></span>

<span data-ttu-id="c09b2-111">Crie um novo VpnServerConfiguration para a conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="c09b2-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="c09b2-112">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="c09b2-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="c09b2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c09b2-113">PARAMETERS</span></span>

### <span data-ttu-id="c09b2-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="c09b2-114">-AadAudience</span></span>
<span data-ttu-id="c09b2-115">Audiência do AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c09b2-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="c09b2-116">-AadIssuer</span></span>
<span data-ttu-id="c09b2-117">Emissor AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c09b2-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="c09b2-118">-AadTenant</span></span>
<span data-ttu-id="c09b2-119">Locatário AAD para autenticação AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c09b2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c09b2-120">-AsJob</span></span>
<span data-ttu-id="c09b2-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c09b2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c09b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09b2-122">-DefaultProfile</span></span>
<span data-ttu-id="c09b2-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c09b2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c09b2-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c09b2-124">-Location</span></span>
<span data-ttu-id="c09b2-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c09b2-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09b2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c09b2-126">-Name</span></span>
<span data-ttu-id="c09b2-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c09b2-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09b2-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c09b2-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="c09b2-129">Uma lista de caminhos dos arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c09b2-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c09b2-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c09b2-130">-RadiusServerAddress</span></span>
<span data-ttu-id="c09b2-131">Endereço do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c09b2-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="c09b2-132">-RadiusServerList</span></span>
<span data-ttu-id="c09b2-133">Servidores de vários raios externos P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="c09b2-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c09b2-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="c09b2-135">Uma lista de caminhos dos arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c09b2-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c09b2-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c09b2-136">-RadiusServerSecret</span></span>
<span data-ttu-id="c09b2-137">Segredo do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="c09b2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c09b2-138">-ResourceGroupName</span></span>
<span data-ttu-id="c09b2-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c09b2-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09b2-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="c09b2-140">-Tag</span></span>
<span data-ttu-id="c09b2-141">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c09b2-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c09b2-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c09b2-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="c09b2-143">A lista de protocolos de túnel de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c09b2-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c09b2-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c09b2-145">Uma lista de políticas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c09b2-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09b2-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c09b2-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="c09b2-147">Uma lista de VpnClientCertificates a serem revogados caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="c09b2-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="c09b2-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c09b2-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="c09b2-149">Uma lista de VpnClientRootCertificates a serem adicionados caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="c09b2-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="c09b2-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="c09b2-150">-VpnProtocol</span></span>
<span data-ttu-id="c09b2-151">A lista de protocolos de túnel de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="c09b2-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c09b2-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c09b2-152">-Confirm</span></span>
<span data-ttu-id="c09b2-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c09b2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c09b2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c09b2-154">-WhatIf</span></span>
<span data-ttu-id="c09b2-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c09b2-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c09b2-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c09b2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c09b2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09b2-157">CommonParameters</span></span>
<span data-ttu-id="c09b2-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c09b2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09b2-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c09b2-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09b2-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c09b2-160">INPUTS</span></span>

### <span data-ttu-id="c09b2-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c09b2-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="c09b2-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c09b2-162">OUTPUTS</span></span>

### <span data-ttu-id="c09b2-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c09b2-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c09b2-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="c09b2-164">NOTES</span></span>

## <span data-ttu-id="c09b2-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c09b2-165">RELATED LINKS</span></span>
