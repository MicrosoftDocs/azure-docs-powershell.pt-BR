---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426927"
---
# <span data-ttu-id="704b8-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="704b8-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="704b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="704b8-102">SYNOPSIS</span></span>
<span data-ttu-id="704b8-103">Criar um objeto PSFrontendEndpoint para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="704b8-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="704b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="704b8-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="704b8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="704b8-105">DESCRIPTION</span></span>
<span data-ttu-id="704b8-106">Criar um objeto PSFrontendEndpoint para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="704b8-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="704b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="704b8-107">EXAMPLES</span></span>

### <span data-ttu-id="704b8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="704b8-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="704b8-109">Crie um objeto PSFrontendEndpoint para a criação da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="704b8-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="704b8-110">OS</span><span class="sxs-lookup"><span data-stu-id="704b8-110">PARAMETERS</span></span>

### <span data-ttu-id="704b8-111">-Certificado</span><span class="sxs-lookup"><span data-stu-id="704b8-111">-CertificateSource</span></span>
<span data-ttu-id="704b8-112">A fonte do certificado SSL</span><span class="sxs-lookup"><span data-stu-id="704b8-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="704b8-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="704b8-113">-CertificateType</span></span>
<span data-ttu-id="704b8-114">o tipo do certificado usado para conexões seguras a um frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="704b8-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="704b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704b8-115">-DefaultProfile</span></span>
<span data-ttu-id="704b8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="704b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704b8-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="704b8-117">-HostName</span></span>
<span data-ttu-id="704b8-118">O nome do host do frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="704b8-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="704b8-119">Deve ser um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="704b8-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="704b8-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="704b8-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="704b8-121">A versão mínima do TLS necessária dos clientes para estabelecer um handshake SSL com a porta frontal.</span><span class="sxs-lookup"><span data-stu-id="704b8-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="704b8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="704b8-122">-Name</span></span>
<span data-ttu-id="704b8-123">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="704b8-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="704b8-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="704b8-124">-ProtocolType</span></span>
<span data-ttu-id="704b8-125">O protocolo de extensão TLS usado para a entrega segura</span><span class="sxs-lookup"><span data-stu-id="704b8-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="704b8-126">-Secretname</span><span class="sxs-lookup"><span data-stu-id="704b8-126">-SecretName</span></span>
<span data-ttu-id="704b8-127">O nome do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="704b8-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="704b8-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="704b8-128">-SecretVersion</span></span>
<span data-ttu-id="704b8-129">A versão do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="704b8-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="704b8-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="704b8-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="704b8-131">Se a afinidade de sessão deve ser permitida neste host.</span><span class="sxs-lookup"><span data-stu-id="704b8-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="704b8-132">O valor padrão está desabilitado</span><span class="sxs-lookup"><span data-stu-id="704b8-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704b8-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="704b8-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="704b8-134">O TTL a ser usado em segundos para afinidade de sessão, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="704b8-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="704b8-135">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="704b8-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="704b8-136">-Cofre</span><span class="sxs-lookup"><span data-stu-id="704b8-136">-Vault</span></span>
<span data-ttu-id="704b8-137">O cofre de chaves que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="704b8-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="704b8-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="704b8-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="704b8-139">A ID do recurso da política de firewall de aplicativo Web para cada host (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="704b8-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="704b8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704b8-140">CommonParameters</span></span>
<span data-ttu-id="704b8-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704b8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704b8-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="704b8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704b8-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="704b8-143">INPUTS</span></span>

### <span data-ttu-id="704b8-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="704b8-144">None</span></span>
## <span data-ttu-id="704b8-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="704b8-145">OUTPUTS</span></span>

### <span data-ttu-id="704b8-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="704b8-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="704b8-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="704b8-147">NOTES</span></span>

## <span data-ttu-id="704b8-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="704b8-148">RELATED LINKS</span></span>

<span data-ttu-id="704b8-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="704b8-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
