---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889533"
---
# <span data-ttu-id="acdae-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="acdae-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="acdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdae-102">SYNOPSIS</span></span>
<span data-ttu-id="acdae-103">Atualize um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="acdae-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="acdae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="acdae-104">SYNTAX</span></span>

### <span data-ttu-id="acdae-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="acdae-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acdae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="acdae-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acdae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="acdae-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acdae-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="acdae-108">DESCRIPTION</span></span>
<span data-ttu-id="acdae-109">Atualize um grupo de registro em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="acdae-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="acdae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acdae-110">EXAMPLES</span></span>

### <span data-ttu-id="acdae-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="acdae-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="acdae-112">Atualize a política de alocação e os hubs para um grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="acdae-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="acdae-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="acdae-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="acdae-114">Atualize o estado duplo inicial de um grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="acdae-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="acdae-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="acdae-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="acdae-116">Atualizar as chaves primárias e secundárias de um grupo de registro de chave simétrica</span><span class="sxs-lookup"><span data-stu-id="acdae-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="acdae-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="acdae-117">PARAMETERS</span></span>

### <span data-ttu-id="acdae-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="acdae-118">-AllocationPolicy</span></span>
<span data-ttu-id="acdae-119">Tipo de alocação para dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="acdae-119">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="acdae-120">-ApiVersion</span></span>
<span data-ttu-id="acdae-121">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="acdae-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="acdae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdae-122">-DefaultProfile</span></span>
<span data-ttu-id="acdae-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acdae-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acdae-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="acdae-124">-Desired</span></span>
<span data-ttu-id="acdae-125">Propriedades iniciais desejadas para o irmão duplo.</span><span class="sxs-lookup"><span data-stu-id="acdae-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="acdae-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="acdae-126">-DpsName</span></span>
<span data-ttu-id="acdae-127">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="acdae-127">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="acdae-128">-DpsObject</span></span>
<span data-ttu-id="acdae-129">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="acdae-129">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="acdae-130">-EdgeEnabled</span></span>
<span data-ttu-id="acdae-131">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="acdae-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="acdae-132">-IotHub</span></span>
<span data-ttu-id="acdae-133">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="acdae-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="acdae-134">Use a lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="acdae-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="acdae-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="acdae-135">-IotHubHostName</span></span>
<span data-ttu-id="acdae-136">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="acdae-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="acdae-137">-Name</span><span class="sxs-lookup"><span data-stu-id="acdae-137">-Name</span></span>
<span data-ttu-id="acdae-138">Nome do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="acdae-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="acdae-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="acdae-139">-PrimaryCAName</span></span>
<span data-ttu-id="acdae-140">O nome do certificado ca raiz principal.</span><span class="sxs-lookup"><span data-stu-id="acdae-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="acdae-141">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="acdae-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="acdae-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="acdae-142">-PrimaryCertificate</span></span>
<span data-ttu-id="acdae-143">O caminho para o arquivo que contém o certificado principal.</span><span class="sxs-lookup"><span data-stu-id="acdae-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="acdae-144">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="acdae-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="acdae-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="acdae-145">-PrimaryKey</span></span>
<span data-ttu-id="acdae-146">A chave de acesso compartilhado simétrica principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="acdae-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="acdae-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="acdae-147">-ProvisioningStatus</span></span>
<span data-ttu-id="acdae-148">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="acdae-148">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="acdae-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="acdae-150">Dados do dispositivo a serem tratados na re provisionamento para hub de Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="acdae-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdae-151">-ResourceGroupName</span></span>
<span data-ttu-id="acdae-152">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="acdae-152">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acdae-153">-ResourceId</span></span>
<span data-ttu-id="acdae-154">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="acdae-154">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdae-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="acdae-155">-RootCertificate</span></span>
<span data-ttu-id="acdae-156">Permite criar x509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="acdae-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="acdae-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="acdae-157">-SecondaryCAName</span></span>
<span data-ttu-id="acdae-158">O nome do certificado ca raiz secundário.</span><span class="sxs-lookup"><span data-stu-id="acdae-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="acdae-159">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="acdae-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="acdae-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="acdae-160">-SecondaryCertificate</span></span>
<span data-ttu-id="acdae-161">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="acdae-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="acdae-162">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="acdae-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="acdae-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="acdae-163">-SecondaryKey</span></span>
<span data-ttu-id="acdae-164">A chave de acesso compartilhado simétrica secundária armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="acdae-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="acdae-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="acdae-165">-Tag</span></span>
<span data-ttu-id="acdae-166">Marcas duplas iniciais.</span><span class="sxs-lookup"><span data-stu-id="acdae-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="acdae-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="acdae-167">-WebhookUrl</span></span>
<span data-ttu-id="acdae-168">A URL de webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="acdae-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="acdae-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acdae-169">-Confirm</span></span>
<span data-ttu-id="acdae-170">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acdae-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acdae-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acdae-171">-WhatIf</span></span>
<span data-ttu-id="acdae-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acdae-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acdae-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acdae-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acdae-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdae-174">CommonParameters</span></span>
<span data-ttu-id="acdae-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acdae-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdae-176">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdae-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdae-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acdae-177">INPUTS</span></span>

### <span data-ttu-id="acdae-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="acdae-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="acdae-179">System.String</span><span class="sxs-lookup"><span data-stu-id="acdae-179">System.String</span></span>

## <span data-ttu-id="acdae-180">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="acdae-180">OUTPUTS</span></span>

### <span data-ttu-id="acdae-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="acdae-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="acdae-182">NOTES</span><span class="sxs-lookup"><span data-stu-id="acdae-182">NOTES</span></span>

## <span data-ttu-id="acdae-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acdae-183">RELATED LINKS</span></span>
