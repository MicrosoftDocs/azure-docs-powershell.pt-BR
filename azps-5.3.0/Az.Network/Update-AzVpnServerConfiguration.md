---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434590"
---
# <span data-ttu-id="b2878-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2878-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b2878-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2878-102">SYNOPSIS</span></span>
<span data-ttu-id="b2878-103">Atualiza um VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="b2878-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="b2878-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2878-104">SYNTAX</span></span>

### <span data-ttu-id="b2878-105">ByVpnServerConfigurationNameByCertificateAuthentication (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2878-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2878-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2878-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2878-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2878-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2878-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2878-114">DESCRIPTION</span></span>
<span data-ttu-id="b2878-115">O cmdlet **Update-AzVpnServerConfiguration** permite que você atualize o VpnServerConfiguration existente com diferentes VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e defina parâmetros relacionados ao tipo de autenticação VPN selecionado, conforme a necessidade do cliente para a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="b2878-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="b2878-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2878-116">EXAMPLES</span></span>

### <span data-ttu-id="b2878-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2878-117">Example 1</span></span>
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

<span data-ttu-id="b2878-118">O comando acima atualizará um VpnServerConfiguration existente com VpnProtocol como IkeV2.</span><span class="sxs-lookup"><span data-stu-id="b2878-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="b2878-119">OS</span><span class="sxs-lookup"><span data-stu-id="b2878-119">PARAMETERS</span></span>

### <span data-ttu-id="b2878-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="b2878-120">-AadAudience</span></span>
<span data-ttu-id="b2878-121">Audiência do AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="b2878-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="b2878-122">-AadIssuer</span></span>
<span data-ttu-id="b2878-123">Emissor AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="b2878-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="b2878-124">-AadTenant</span></span>
<span data-ttu-id="b2878-125">Locatário AAD para autenticação P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="b2878-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2878-126">-AsJob</span></span>
<span data-ttu-id="b2878-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2878-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2878-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2878-128">-DefaultProfile</span></span>
<span data-ttu-id="b2878-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2878-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2878-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2878-130">-InputObject</span></span>
<span data-ttu-id="b2878-131">O objeto de configuração do servidor VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="b2878-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2878-132">-Name</span></span>
<span data-ttu-id="b2878-133">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b2878-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b2878-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="b2878-135">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b2878-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b2878-136">-RadiusServerAddress</span></span>
<span data-ttu-id="b2878-137">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="b2878-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="b2878-138">-RadiusServerList</span></span>
<span data-ttu-id="b2878-139">P2S vários servidores externos RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2878-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b2878-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="b2878-141">Uma lista de caminhos de arquivos RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b2878-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b2878-142">-RadiusServerSecret</span></span>
<span data-ttu-id="b2878-143">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="b2878-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2878-144">-ResourceGroupName</span></span>
<span data-ttu-id="b2878-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2878-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2878-146">-ResourceId</span></span>
<span data-ttu-id="b2878-147">A ID de recurso do Azure para a configuração do servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="b2878-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2878-148">-Tag</span></span>
<span data-ttu-id="b2878-149">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2878-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b2878-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b2878-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="b2878-151">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="b2878-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="b2878-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b2878-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b2878-153">Uma lista de diretivas IPSec para VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2878-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="b2878-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b2878-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="b2878-155">Uma lista de caminhos dos arquivos VpnClientCertificates a serem revogados</span><span class="sxs-lookup"><span data-stu-id="b2878-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b2878-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="b2878-157">Uma lista de caminhos dos arquivos VpnClientRootCertificates para adicionar arquivos</span><span class="sxs-lookup"><span data-stu-id="b2878-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2878-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="b2878-158">-VpnProtocol</span></span>
<span data-ttu-id="b2878-159">A lista de protocolos de encapsulamento de cliente VPN da P2S.</span><span class="sxs-lookup"><span data-stu-id="b2878-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="b2878-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2878-160">-Confirm</span></span>
<span data-ttu-id="b2878-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2878-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2878-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2878-162">-WhatIf</span></span>
<span data-ttu-id="b2878-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2878-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2878-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2878-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2878-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2878-165">CommonParameters</span></span>
<span data-ttu-id="b2878-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2878-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2878-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2878-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2878-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2878-168">INPUTS</span></span>

### <span data-ttu-id="b2878-169">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2878-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="b2878-170">System. String Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="b2878-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="b2878-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2878-171">OUTPUTS</span></span>

### <span data-ttu-id="b2878-172">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2878-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b2878-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2878-173">NOTES</span></span>

## <span data-ttu-id="b2878-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2878-174">RELATED LINKS</span></span>
