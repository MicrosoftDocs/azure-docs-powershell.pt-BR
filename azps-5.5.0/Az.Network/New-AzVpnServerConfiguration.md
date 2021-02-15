---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117366"
---
# <span data-ttu-id="1036b-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1036b-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="1036b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1036b-102">SYNOPSIS</span></span>
<span data-ttu-id="1036b-103">Crie uma nova VpnServerConfiguration para apontar para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="1036b-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="1036b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1036b-104">SYNTAX</span></span>

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

## <span data-ttu-id="1036b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1036b-105">DESCRIPTION</span></span>
<span data-ttu-id="1036b-106">O cmdlet **New-AzVpnServerConfiguration** permite que você crie uma nova VpnServerConfiguration com diferentes vpnProtocols, VpnAuthenticationTypes, IpsecPolicies e definir parâmetros relacionados ao tipo de autenticação de vpn selecionado de acordo com o requisito do cliente para a conectividade apontar para o site.</span><span class="sxs-lookup"><span data-stu-id="1036b-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="1036b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1036b-107">EXAMPLES</span></span>

### <span data-ttu-id="1036b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1036b-108">Example 1</span></span>
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

<span data-ttu-id="1036b-109">O comando acima criará um novo VpnServerConfiguration com VpnAuthenticationType como Certificado.</span><span class="sxs-lookup"><span data-stu-id="1036b-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="1036b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1036b-110">Example 2</span></span>

<span data-ttu-id="1036b-111">Crie uma nova VpnServerConfiguration para apontar para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="1036b-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="1036b-112">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="1036b-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="1036b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1036b-113">PARAMETERS</span></span>

### <span data-ttu-id="1036b-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="1036b-114">-AadAudience</span></span>
<span data-ttu-id="1036b-115">Audiência do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1036b-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1036b-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="1036b-116">-AadIssuer</span></span>
<span data-ttu-id="1036b-117">Emissor do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1036b-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1036b-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="1036b-118">-AadTenant</span></span>
<span data-ttu-id="1036b-119">Locatário do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="1036b-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1036b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1036b-120">-AsJob</span></span>
<span data-ttu-id="1036b-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1036b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1036b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1036b-122">-DefaultProfile</span></span>
<span data-ttu-id="1036b-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1036b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1036b-124">-Local</span><span class="sxs-lookup"><span data-stu-id="1036b-124">-Location</span></span>
<span data-ttu-id="1036b-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1036b-125">The resource location.</span></span>

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

### <span data-ttu-id="1036b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1036b-126">-Name</span></span>
<span data-ttu-id="1036b-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1036b-127">The resource name.</span></span>

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

### <span data-ttu-id="1036b-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1036b-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="1036b-129">Uma lista dos caminhos dos arquivos de RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1036b-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="1036b-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1036b-130">-RadiusServerAddress</span></span>
<span data-ttu-id="1036b-131">Endereço do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="1036b-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="1036b-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="1036b-132">-RadiusServerList</span></span>
<span data-ttu-id="1036b-133">P2S Servidores externos de múltiplos raios.</span><span class="sxs-lookup"><span data-stu-id="1036b-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="1036b-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1036b-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="1036b-135">Uma lista dos caminhos dos arquivos de RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1036b-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="1036b-136">-RadiusServerSecsec</span><span class="sxs-lookup"><span data-stu-id="1036b-136">-RadiusServerSecret</span></span>
<span data-ttu-id="1036b-137">Segredo do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="1036b-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="1036b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1036b-138">-ResourceGroupName</span></span>
<span data-ttu-id="1036b-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1036b-139">The resource group name.</span></span>

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

### <span data-ttu-id="1036b-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="1036b-140">-Tag</span></span>
<span data-ttu-id="1036b-141">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="1036b-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1036b-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1036b-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="1036b-143">A lista de protocolos de túnel do cliente P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="1036b-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1036b-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1036b-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1036b-145">Uma lista de políticas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1036b-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="1036b-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1036b-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="1036b-147">Uma lista de VpnClientCertificates a serem revogados caminhos de arquivos</span><span class="sxs-lookup"><span data-stu-id="1036b-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="1036b-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1036b-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="1036b-149">Uma lista de VpnClientRootCertificates para adicionar os caminhos dos arquivos</span><span class="sxs-lookup"><span data-stu-id="1036b-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="1036b-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="1036b-150">-VpnProtocol</span></span>
<span data-ttu-id="1036b-151">A lista de protocolos de túnel do cliente P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="1036b-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1036b-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1036b-152">-Confirm</span></span>
<span data-ttu-id="1036b-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1036b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1036b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1036b-154">-WhatIf</span></span>
<span data-ttu-id="1036b-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1036b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1036b-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1036b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1036b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1036b-157">CommonParameters</span></span>
<span data-ttu-id="1036b-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1036b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1036b-159">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1036b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1036b-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="1036b-160">INPUTS</span></span>

### <span data-ttu-id="1036b-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="1036b-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="1036b-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="1036b-162">OUTPUTS</span></span>

### <span data-ttu-id="1036b-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1036b-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1036b-164">Notas</span><span class="sxs-lookup"><span data-stu-id="1036b-164">NOTES</span></span>

## <span data-ttu-id="1036b-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1036b-165">RELATED LINKS</span></span>
