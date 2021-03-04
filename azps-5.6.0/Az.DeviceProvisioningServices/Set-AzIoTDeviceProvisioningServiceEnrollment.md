---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889534"
---
# <span data-ttu-id="988d6-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="988d6-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="988d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988d6-102">SYNOPSIS</span></span>
<span data-ttu-id="988d6-103">Atualizar um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="988d6-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="988d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="988d6-104">SYNTAX</span></span>

### <span data-ttu-id="988d6-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="988d6-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988d6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="988d6-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988d6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="988d6-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="988d6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="988d6-108">DESCRIPTION</span></span>
<span data-ttu-id="988d6-109">Atualize um registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="988d6-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="988d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="988d6-110">EXAMPLES</span></span>

### <span data-ttu-id="988d6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="988d6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="988d6-112">Atualize a política de alocação e os hubs para um registro de registro.</span><span class="sxs-lookup"><span data-stu-id="988d6-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="988d6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="988d6-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="988d6-114">Atualize o estado duplo inicial de um registro.</span><span class="sxs-lookup"><span data-stu-id="988d6-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="988d6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="988d6-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="988d6-116">Atualizar certificados primários e secundários de um registro de chave simétrica</span><span class="sxs-lookup"><span data-stu-id="988d6-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="988d6-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="988d6-117">PARAMETERS</span></span>

### <span data-ttu-id="988d6-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="988d6-118">-AllocationPolicy</span></span>
<span data-ttu-id="988d6-119">Tipo de alocação para dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="988d6-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="988d6-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="988d6-120">-ApiVersion</span></span>
<span data-ttu-id="988d6-121">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="988d6-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="988d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988d6-122">-DefaultProfile</span></span>
<span data-ttu-id="988d6-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="988d6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988d6-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="988d6-124">-Desired</span></span>
<span data-ttu-id="988d6-125">Propriedades iniciais desejadas para o irmão duplo.</span><span class="sxs-lookup"><span data-stu-id="988d6-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="988d6-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="988d6-126">-DeviceId</span></span>
<span data-ttu-id="988d6-127">ID do dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="988d6-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="988d6-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="988d6-128">-DpsName</span></span>
<span data-ttu-id="988d6-129">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="988d6-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="988d6-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="988d6-130">-DpsObject</span></span>
<span data-ttu-id="988d6-131">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="988d6-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="988d6-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="988d6-132">-EdgeEnabled</span></span>
<span data-ttu-id="988d6-133">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="988d6-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="988d6-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="988d6-134">-EndorsementKey</span></span>
<span data-ttu-id="988d6-135">Chave de endosso do TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="988d6-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="988d6-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="988d6-136">-IotHub</span></span>
<span data-ttu-id="988d6-137">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="988d6-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="988d6-138">Use a lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="988d6-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="988d6-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="988d6-139">-IotHubHostName</span></span>
<span data-ttu-id="988d6-140">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="988d6-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="988d6-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="988d6-141">-PrimaryCAName</span></span>
<span data-ttu-id="988d6-142">O nome do certificado ca raiz principal.</span><span class="sxs-lookup"><span data-stu-id="988d6-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="988d6-143">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="988d6-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="988d6-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="988d6-144">-PrimaryCertificate</span></span>
<span data-ttu-id="988d6-145">O caminho para o arquivo que contém o certificado principal.</span><span class="sxs-lookup"><span data-stu-id="988d6-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="988d6-146">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="988d6-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="988d6-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="988d6-147">-PrimaryKey</span></span>
<span data-ttu-id="988d6-148">A chave de acesso compartilhado simétrica principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="988d6-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="988d6-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="988d6-149">-ProvisioningStatus</span></span>
<span data-ttu-id="988d6-150">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="988d6-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="988d6-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="988d6-151">-RegistrationId</span></span>
<span data-ttu-id="988d6-152">ID de registro de registro individual.</span><span class="sxs-lookup"><span data-stu-id="988d6-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="988d6-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="988d6-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="988d6-154">Dados do dispositivo a serem tratados na re provisionamento para hub de Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="988d6-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="988d6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988d6-155">-ResourceGroupName</span></span>
<span data-ttu-id="988d6-156">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="988d6-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="988d6-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="988d6-157">-ResourceId</span></span>
<span data-ttu-id="988d6-158">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="988d6-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="988d6-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="988d6-159">-RootCertificate</span></span>
<span data-ttu-id="988d6-160">Alternar para atualizar x509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="988d6-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="988d6-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="988d6-161">-SecondaryCAName</span></span>
<span data-ttu-id="988d6-162">O nome do certificado ca raiz secundário.</span><span class="sxs-lookup"><span data-stu-id="988d6-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="988d6-163">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="988d6-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="988d6-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="988d6-164">-SecondaryCertificate</span></span>
<span data-ttu-id="988d6-165">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="988d6-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="988d6-166">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="988d6-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="988d6-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="988d6-167">-SecondaryKey</span></span>
<span data-ttu-id="988d6-168">A chave de acesso compartilhado simétrica secundária armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="988d6-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="988d6-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="988d6-169">-StorageRootKey</span></span>
<span data-ttu-id="988d6-170">Chave raiz de armazenamento TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="988d6-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="988d6-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="988d6-171">-Tag</span></span>
<span data-ttu-id="988d6-172">Marcas duplas iniciais.</span><span class="sxs-lookup"><span data-stu-id="988d6-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="988d6-173">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="988d6-173">-WebhookUrl</span></span>
<span data-ttu-id="988d6-174">A URL de webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="988d6-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="988d6-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="988d6-175">-Confirm</span></span>
<span data-ttu-id="988d6-176">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988d6-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988d6-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988d6-177">-WhatIf</span></span>
<span data-ttu-id="988d6-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="988d6-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988d6-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="988d6-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988d6-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988d6-180">CommonParameters</span></span>
<span data-ttu-id="988d6-181">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988d6-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988d6-182">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988d6-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988d6-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="988d6-183">INPUTS</span></span>

### <span data-ttu-id="988d6-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="988d6-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="988d6-185">System.String</span><span class="sxs-lookup"><span data-stu-id="988d6-185">System.String</span></span>

## <span data-ttu-id="988d6-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="988d6-186">OUTPUTS</span></span>

### <span data-ttu-id="988d6-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="988d6-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="988d6-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="988d6-188">NOTES</span></span>

## <span data-ttu-id="988d6-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="988d6-189">RELATED LINKS</span></span>
