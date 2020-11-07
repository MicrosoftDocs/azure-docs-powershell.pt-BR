---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 6d6253b338bef04c39032bb29b5fb0ba300f4073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770865"
---
# <span data-ttu-id="0b183-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0b183-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="0b183-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b183-102">SYNOPSIS</span></span>
<span data-ttu-id="0b183-103">Criar um objeto PSFrontendEndpoint para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="0b183-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0b183-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b183-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b183-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b183-105">DESCRIPTION</span></span>
<span data-ttu-id="0b183-106">Criar um objeto PSFrontendEndpoint para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="0b183-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0b183-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b183-107">EXAMPLES</span></span>

### <span data-ttu-id="0b183-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b183-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="0b183-109">Criar um objeto PSFrontendEndpoint para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="0b183-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0b183-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b183-110">PARAMETERS</span></span>

### <span data-ttu-id="0b183-111">-Certificado</span><span class="sxs-lookup"><span data-stu-id="0b183-111">-CertificateSource</span></span>
<span data-ttu-id="0b183-112">A fonte do certificado SSL</span><span class="sxs-lookup"><span data-stu-id="0b183-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="0b183-113">-CertificateType</span></span>
<span data-ttu-id="0b183-114">o tipo do certificado usado para conexões seguras a um frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b183-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b183-115">-DefaultProfile</span></span>
<span data-ttu-id="0b183-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b183-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b183-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="0b183-117">-HostName</span></span>
<span data-ttu-id="0b183-118">O nome do host do frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0b183-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="0b183-119">Deve ser um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="0b183-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="0b183-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b183-120">-Name</span></span>
<span data-ttu-id="0b183-121">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="0b183-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="0b183-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="0b183-122">-ProtocolType</span></span>
<span data-ttu-id="0b183-123">O protocolo de extensão TLS usado para a entrega segura</span><span class="sxs-lookup"><span data-stu-id="0b183-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="0b183-124">-SecretName</span></span>
<span data-ttu-id="0b183-125">O nome do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="0b183-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0b183-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="0b183-126">-SecretVersion</span></span>
<span data-ttu-id="0b183-127">A versão do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="0b183-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0b183-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="0b183-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="0b183-129">Se a afinidade de sessão deve ser permitida neste host.</span><span class="sxs-lookup"><span data-stu-id="0b183-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="0b183-130">O valor padrão está desabilitado</span><span class="sxs-lookup"><span data-stu-id="0b183-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="0b183-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b183-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="0b183-132">O TTL a ser usado em segundos para afinidade de sessão, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="0b183-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="0b183-133">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="0b183-133">Default value is 0</span></span>

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

### <span data-ttu-id="0b183-134">-Cofre</span><span class="sxs-lookup"><span data-stu-id="0b183-134">-Vault</span></span>
<span data-ttu-id="0b183-135">O cofre de chaves que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="0b183-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="0b183-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="0b183-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="0b183-137">A ID do recurso da política de firewall de aplicativo Web para cada host (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="0b183-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="0b183-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b183-138">CommonParameters</span></span>
<span data-ttu-id="0b183-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b183-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b183-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b183-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b183-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b183-141">INPUTS</span></span>

### <span data-ttu-id="0b183-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b183-142">None</span></span>

## <span data-ttu-id="0b183-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b183-143">OUTPUTS</span></span>

### <span data-ttu-id="0b183-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b183-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="0b183-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b183-145">NOTES</span></span>

## <span data-ttu-id="0b183-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b183-146">RELATED LINKS</span></span>

<span data-ttu-id="0b183-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0b183-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
