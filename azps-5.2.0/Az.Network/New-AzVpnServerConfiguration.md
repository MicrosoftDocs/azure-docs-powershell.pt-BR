---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260233"
---
# <span data-ttu-id="1e255-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e255-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="1e255-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e255-102">SYNOPSIS</span></span>
<span data-ttu-id="1e255-103">Crie um novo VpnServerConfiguration para o ponto de conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="1e255-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="1e255-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e255-104">SYNTAX</span></span>

### <span data-ttu-id="1e255-105">ByVpnServerConfigurationNameByCertificateAuthentication (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e255-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e255-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e255-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e255-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e255-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e255-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e255-108">DESCRIPTION</span></span>
<span data-ttu-id="1e255-109">O cmdlet **New-AzVpnServerConfiguration** permite que você crie um novo VpnServerConfiguration com diferentes VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e defina parâmetros relacionados ao tipo de autenticação VPN selecionado, conforme a necessidade do cliente para a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="1e255-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="1e255-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e255-110">EXAMPLES</span></span>

### <span data-ttu-id="1e255-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e255-111">Example 1</span></span>
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

<span data-ttu-id="1e255-112">O comando acima criará um novo VpnServerConfiguration com VpnAuthenticationType como certificado.</span><span class="sxs-lookup"><span data-stu-id="1e255-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="1e255-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1e255-113">Example 2</span></span>

<span data-ttu-id="1e255-114">Crie um novo VpnServerConfiguration para o ponto de conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="1e255-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="1e255-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="1e255-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="1e255-116">OS</span><span class="sxs-lookup"><span data-stu-id="1e255-116">PARAMETERS</span></span>

### <span data-ttu-id="1e255-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="1e255-117">-AadAudience</span></span>
<span data-ttu-id="1e255-118">Audiência do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1e255-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="1e255-119">-AadIssuer</span></span>
<span data-ttu-id="1e255-120">Emissor AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1e255-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="1e255-121">-AadTenant</span></span>
<span data-ttu-id="1e255-122">Locatário AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1e255-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e255-123">-AsJob</span></span>
<span data-ttu-id="1e255-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1e255-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e255-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e255-125">-DefaultProfile</span></span>
<span data-ttu-id="1e255-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e255-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e255-127">-Local</span><span class="sxs-lookup"><span data-stu-id="1e255-127">-Location</span></span>
<span data-ttu-id="1e255-128">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e255-128">The resource location.</span></span>

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

### <span data-ttu-id="1e255-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e255-129">-Name</span></span>
<span data-ttu-id="1e255-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e255-130">The resource name.</span></span>

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

### <span data-ttu-id="1e255-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e255-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="1e255-132">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e255-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1e255-133">-RadiusServerAddress</span></span>
<span data-ttu-id="1e255-134">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="1e255-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="1e255-135">-RadiusServerList</span></span>
<span data-ttu-id="1e255-136">P2S vários servidores externos RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1e255-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e255-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="1e255-138">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e255-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1e255-139">-RadiusServerSecret</span></span>
<span data-ttu-id="1e255-140">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="1e255-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e255-141">-ResourceGroupName</span></span>
<span data-ttu-id="1e255-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e255-142">The resource group name.</span></span>

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

### <span data-ttu-id="1e255-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="1e255-143">-Tag</span></span>
<span data-ttu-id="1e255-144">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e255-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1e255-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1e255-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="1e255-146">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="1e255-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1e255-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1e255-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1e255-148">Uma lista de diretivas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e255-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="1e255-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e255-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="1e255-150">Uma lista de caminhos dos arquivos VpnClientCertificates a serem revogados</span><span class="sxs-lookup"><span data-stu-id="1e255-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e255-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="1e255-152">Uma lista de caminhos dos arquivos VpnClientRootCertificates para adicionar arquivos</span><span class="sxs-lookup"><span data-stu-id="1e255-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e255-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="1e255-153">-VpnProtocol</span></span>
<span data-ttu-id="1e255-154">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="1e255-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1e255-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e255-155">-Confirm</span></span>
<span data-ttu-id="1e255-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e255-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e255-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e255-157">-WhatIf</span></span>
<span data-ttu-id="1e255-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e255-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e255-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e255-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e255-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e255-160">CommonParameters</span></span>
<span data-ttu-id="1e255-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e255-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e255-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e255-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e255-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e255-163">INPUTS</span></span>

### <span data-ttu-id="1e255-164">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="1e255-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="1e255-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e255-165">OUTPUTS</span></span>

### <span data-ttu-id="1e255-166">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e255-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1e255-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e255-167">NOTES</span></span>

## <span data-ttu-id="1e255-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e255-168">RELATED LINKS</span></span>
