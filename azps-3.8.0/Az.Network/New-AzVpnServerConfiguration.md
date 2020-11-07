---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778072"
---
# <span data-ttu-id="c949b-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c949b-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c949b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c949b-102">SYNOPSIS</span></span>
<span data-ttu-id="c949b-103">Crie um novo VpnServerConfiguration para o ponto de conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="c949b-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c949b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c949b-104">SYNTAX</span></span>

### <span data-ttu-id="c949b-105">ByVpnServerConfigurationNameByCertificateAuthentication (padrão)</span><span class="sxs-lookup"><span data-stu-id="c949b-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c949b-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="c949b-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c949b-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="c949b-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c949b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c949b-108">DESCRIPTION</span></span>
<span data-ttu-id="c949b-109">O cmdlet **New-AzVpnServerConfiguration** permite que você crie um novo VpnServerConfiguration com diferentes VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e defina parâmetros relacionados ao tipo de autenticação VPN selecionado, conforme a necessidade do cliente para a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="c949b-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="c949b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c949b-110">EXAMPLES</span></span>

### <span data-ttu-id="c949b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c949b-111">Example 1</span></span>
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

<span data-ttu-id="c949b-112">O comando acima criará um novo VpnServerConfiguration com VpnAuthenticationType como certificado.</span><span class="sxs-lookup"><span data-stu-id="c949b-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="c949b-113">OS</span><span class="sxs-lookup"><span data-stu-id="c949b-113">PARAMETERS</span></span>

### <span data-ttu-id="c949b-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="c949b-114">-AadAudience</span></span>
<span data-ttu-id="c949b-115">Audiência do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="c949b-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="c949b-116">-AadIssuer</span></span>
<span data-ttu-id="c949b-117">Emissor AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="c949b-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="c949b-118">-AadTenant</span></span>
<span data-ttu-id="c949b-119">Locatário AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="c949b-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c949b-120">-AsJob</span></span>
<span data-ttu-id="c949b-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c949b-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c949b-122">-DefaultProfile</span></span>
<span data-ttu-id="c949b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c949b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-124">-Local</span><span class="sxs-lookup"><span data-stu-id="c949b-124">-Location</span></span>
<span data-ttu-id="c949b-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c949b-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c949b-126">-Name</span></span>
<span data-ttu-id="c949b-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c949b-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c949b-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="c949b-129">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c949b-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c949b-130">-RadiusServerAddress</span></span>
<span data-ttu-id="c949b-131">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="c949b-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c949b-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="c949b-133">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c949b-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c949b-134">-RadiusServerSecret</span></span>
<span data-ttu-id="c949b-135">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="c949b-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c949b-136">-ResourceGroupName</span></span>
<span data-ttu-id="c949b-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c949b-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="c949b-138">-Tag</span></span>
<span data-ttu-id="c949b-139">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="c949b-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c949b-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="c949b-141">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="c949b-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c949b-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c949b-143">Uma lista de diretivas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c949b-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c949b-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="c949b-145">Uma lista de caminhos dos arquivos VpnClientCertificates a serem revogados</span><span class="sxs-lookup"><span data-stu-id="c949b-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c949b-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="c949b-147">Uma lista de caminhos dos arquivos VpnClientRootCertificates para adicionar arquivos</span><span class="sxs-lookup"><span data-stu-id="c949b-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="c949b-148">-VpnProtocol</span></span>
<span data-ttu-id="c949b-149">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="c949b-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c949b-150">-Confirm</span></span>
<span data-ttu-id="c949b-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c949b-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c949b-152">-WhatIf</span></span>
<span data-ttu-id="c949b-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c949b-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c949b-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c949b-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c949b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c949b-155">CommonParameters</span></span>
<span data-ttu-id="c949b-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c949b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c949b-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c949b-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c949b-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c949b-158">INPUTS</span></span>

### <span data-ttu-id="c949b-159">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="c949b-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="c949b-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c949b-160">OUTPUTS</span></span>

### <span data-ttu-id="c949b-161">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c949b-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c949b-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c949b-162">NOTES</span></span>

## <span data-ttu-id="c949b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c949b-163">RELATED LINKS</span></span>
