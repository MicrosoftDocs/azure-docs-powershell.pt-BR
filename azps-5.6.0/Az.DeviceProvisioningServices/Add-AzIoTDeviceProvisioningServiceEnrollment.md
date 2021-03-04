---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 5aca36433089a2e84965ee6d1d8b2c17d3c53205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887992"
---
# <span data-ttu-id="bc5ec-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="bc5ec-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="bc5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5ec-103">Crie um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="bc5ec-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc5ec-104">SYNTAX</span></span>

### <span data-ttu-id="bc5ec-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc5ec-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc5ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bc5ec-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc5ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bc5ec-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5ec-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc5ec-108">DESCRIPTION</span></span>
<span data-ttu-id="bc5ec-109">Crie um registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="bc5ec-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-110">EXAMPLES</span></span>

### <span data-ttu-id="bc5ec-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc5ec-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="bc5ec-112">Criar um registro com o tipo de atestado SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="bc5ec-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="bc5ec-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bc5ec-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="bc5ec-114">Crie um registro com atestado do TPM.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="bc5ec-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bc5ec-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="bc5ec-116">Criar um registro com o tipo de atestado X509</span><span class="sxs-lookup"><span data-stu-id="bc5ec-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="bc5ec-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bc5ec-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="bc5ec-118">Crie um registro com o tipo de atestado SymmetricKey e estado duplo inicial.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="bc5ec-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-119">PARAMETERS</span></span>

### <span data-ttu-id="bc5ec-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bc5ec-120">-AllocationPolicy</span></span>
<span data-ttu-id="bc5ec-121">Tipo de alocação para dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="bc5ec-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc5ec-122">-ApiVersion</span></span>
<span data-ttu-id="bc5ec-123">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="bc5ec-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="bc5ec-124">-AttestationType</span></span>
<span data-ttu-id="bc5ec-125">Mecanismo de atestado.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-125">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5ec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5ec-126">-DefaultProfile</span></span>
<span data-ttu-id="bc5ec-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc5ec-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="bc5ec-128">-Desired</span></span>
<span data-ttu-id="bc5ec-129">Propriedades iniciais desejadas para o irmão duplo.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="bc5ec-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bc5ec-130">-DeviceId</span></span>
<span data-ttu-id="bc5ec-131">ID do dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="bc5ec-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="bc5ec-132">-DpsName</span></span>
<span data-ttu-id="bc5ec-133">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="bc5ec-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bc5ec-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="bc5ec-134">-DpsObject</span></span>
<span data-ttu-id="bc5ec-135">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="bc5ec-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bc5ec-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="bc5ec-136">-EdgeEnabled</span></span>
<span data-ttu-id="bc5ec-137">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="bc5ec-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="bc5ec-138">-EndorsementKey</span></span>
<span data-ttu-id="bc5ec-139">Chave de endosso do TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="bc5ec-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="bc5ec-140">-IotHub</span></span>
<span data-ttu-id="bc5ec-141">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="bc5ec-142">Use a lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="bc5ec-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="bc5ec-143">-IotHubHostName</span></span>
<span data-ttu-id="bc5ec-144">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="bc5ec-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="bc5ec-145">-PrimaryCAName</span></span>
<span data-ttu-id="bc5ec-146">O nome do certificado ca raiz principal.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="bc5ec-147">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="bc5ec-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5ec-148">-PrimaryCertificate</span></span>
<span data-ttu-id="bc5ec-149">O caminho para o arquivo que contém o certificado principal.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="bc5ec-150">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="bc5ec-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="bc5ec-151">-PrimaryKey</span></span>
<span data-ttu-id="bc5ec-152">A chave de acesso compartilhado simétrica principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="bc5ec-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="bc5ec-153">-ProvisioningStatus</span></span>
<span data-ttu-id="bc5ec-154">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="bc5ec-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="bc5ec-155">-RegistrationId</span></span>
<span data-ttu-id="bc5ec-156">ID de registro de registro individual.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="bc5ec-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="bc5ec-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="bc5ec-158">Dados do dispositivo a serem tratados na re provisionamento para hub de Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="bc5ec-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5ec-159">-ResourceGroupName</span></span>
<span data-ttu-id="bc5ec-160">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bc5ec-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bc5ec-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc5ec-161">-ResourceId</span></span>
<span data-ttu-id="bc5ec-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="bc5ec-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bc5ec-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5ec-163">-RootCertificate</span></span>
<span data-ttu-id="bc5ec-164">Permite criar x509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="bc5ec-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="bc5ec-165">-SecondaryCAName</span></span>
<span data-ttu-id="bc5ec-166">O nome do certificado ca raiz secundário.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="bc5ec-167">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="bc5ec-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5ec-168">-SecondaryCertificate</span></span>
<span data-ttu-id="bc5ec-169">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="bc5ec-170">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="bc5ec-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="bc5ec-171">-SecondaryKey</span></span>
<span data-ttu-id="bc5ec-172">A chave de acesso compartilhado simétrica secundária armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="bc5ec-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="bc5ec-173">-StorageRootKey</span></span>
<span data-ttu-id="bc5ec-174">Chave raiz de armazenamento TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="bc5ec-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc5ec-175">-Tag</span></span>
<span data-ttu-id="bc5ec-176">Marcas duplas iniciais.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="bc5ec-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="bc5ec-177">-WebhookUrl</span></span>
<span data-ttu-id="bc5ec-178">A URL de webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="bc5ec-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc5ec-179">-Confirm</span></span>
<span data-ttu-id="bc5ec-180">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5ec-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5ec-181">-WhatIf</span></span>
<span data-ttu-id="bc5ec-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5ec-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5ec-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5ec-184">CommonParameters</span></span>
<span data-ttu-id="bc5ec-185">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc5ec-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5ec-186">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5ec-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5ec-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-187">INPUTS</span></span>

### <span data-ttu-id="bc5ec-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bc5ec-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bc5ec-189">System.String</span><span class="sxs-lookup"><span data-stu-id="bc5ec-189">System.String</span></span>

## <span data-ttu-id="bc5ec-190">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-190">OUTPUTS</span></span>

### <span data-ttu-id="bc5ec-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="bc5ec-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="bc5ec-192">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc5ec-192">NOTES</span></span>

## <span data-ttu-id="bc5ec-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc5ec-193">RELATED LINKS</span></span>
