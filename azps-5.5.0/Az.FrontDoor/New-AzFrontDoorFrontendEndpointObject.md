---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116793"
---
# <span data-ttu-id="a8c51-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a8c51-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="a8c51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8c51-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c51-103">Criar um Objeto PSFrontendEndpoint para criação de Porta Frontal</span><span class="sxs-lookup"><span data-stu-id="a8c51-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a8c51-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8c51-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8c51-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8c51-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c51-106">Criar um Objeto PSFrontendEndpoint para criação de Porta Frontal</span><span class="sxs-lookup"><span data-stu-id="a8c51-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a8c51-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8c51-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c51-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8c51-108">Example 1</span></span>
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

<span data-ttu-id="a8c51-109">Crie um Objeto PSFrontendEndpoint para criação de Porta Frontal.</span><span class="sxs-lookup"><span data-stu-id="a8c51-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="a8c51-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8c51-110">PARAMETERS</span></span>

### <span data-ttu-id="a8c51-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="a8c51-111">-CertificateSource</span></span>
<span data-ttu-id="a8c51-112">A origem do certificado SSL</span><span class="sxs-lookup"><span data-stu-id="a8c51-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="a8c51-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="a8c51-113">-CertificateType</span></span>
<span data-ttu-id="a8c51-114">o tipo de certificado usado para conexões seguras com um frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8c51-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="a8c51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c51-115">-DefaultProfile</span></span>
<span data-ttu-id="a8c51-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8c51-117">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="a8c51-117">-HostName</span></span>
<span data-ttu-id="a8c51-118">O nome do host do frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a8c51-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="a8c51-119">Deve ser um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="a8c51-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="a8c51-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a8c51-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="a8c51-121">A versão TLS mínima necessária para os clientes estabelecerem um handshake SSL com o Front Door.</span><span class="sxs-lookup"><span data-stu-id="a8c51-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="a8c51-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8c51-122">-Name</span></span>
<span data-ttu-id="a8c51-123">Nome do ponto de extremidade frontend.</span><span class="sxs-lookup"><span data-stu-id="a8c51-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="a8c51-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a8c51-124">-ProtocolType</span></span>
<span data-ttu-id="a8c51-125">O protocolo de extensão TLS usado para entrega segura</span><span class="sxs-lookup"><span data-stu-id="a8c51-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="a8c51-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="a8c51-126">-SecretName</span></span>
<span data-ttu-id="a8c51-127">O nome do segredo do Cofre de Chaves representando o certificado PFX completo</span><span class="sxs-lookup"><span data-stu-id="a8c51-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a8c51-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a8c51-128">-SecretVersion</span></span>
<span data-ttu-id="a8c51-129">A versão do segredo do Cofre de Chaves representando o certificado PFX completo</span><span class="sxs-lookup"><span data-stu-id="a8c51-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a8c51-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="a8c51-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="a8c51-131">Se você quer permitir affinity de sessão neste host.</span><span class="sxs-lookup"><span data-stu-id="a8c51-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="a8c51-132">O valor padrão está desabilitado</span><span class="sxs-lookup"><span data-stu-id="a8c51-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="a8c51-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a8c51-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="a8c51-134">O TTL a ser usado em segundos para affinidade da sessão, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="a8c51-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="a8c51-135">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="a8c51-135">Default value is 0</span></span>

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

### <span data-ttu-id="a8c51-136">-Cofre</span><span class="sxs-lookup"><span data-stu-id="a8c51-136">-Vault</span></span>
<span data-ttu-id="a8c51-137">O Cofre de Teclas que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="a8c51-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="a8c51-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="a8c51-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="a8c51-139">A ID de recurso da política de Firewall do Aplicativo Web para cada host (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="a8c51-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="a8c51-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c51-140">CommonParameters</span></span>
<span data-ttu-id="a8c51-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c51-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c51-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8c51-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c51-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="a8c51-143">INPUTS</span></span>

### <span data-ttu-id="a8c51-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8c51-144">None</span></span>
## <span data-ttu-id="a8c51-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="a8c51-145">OUTPUTS</span></span>

### <span data-ttu-id="a8c51-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8c51-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="a8c51-147">Notas</span><span class="sxs-lookup"><span data-stu-id="a8c51-147">NOTES</span></span>

## <span data-ttu-id="a8c51-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8c51-148">RELATED LINKS</span></span>

<span data-ttu-id="a8c51-149">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a8c51-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
