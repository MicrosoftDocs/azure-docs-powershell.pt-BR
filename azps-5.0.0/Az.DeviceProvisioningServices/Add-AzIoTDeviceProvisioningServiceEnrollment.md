---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115534"
---
# <span data-ttu-id="7f78c-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="7f78c-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="7f78c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f78c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f78c-103">Crie um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f78c-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="7f78c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f78c-104">SYNTAX</span></span>

### <span data-ttu-id="7f78c-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f78c-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="7f78c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f78c-106">InputObjectSet</span></span>
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

### <span data-ttu-id="7f78c-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="7f78c-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="7f78c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f78c-108">DESCRIPTION</span></span>
<span data-ttu-id="7f78c-109">Crie um registro de dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f78c-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7f78c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f78c-110">EXAMPLES</span></span>

### <span data-ttu-id="7f78c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f78c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="7f78c-112">Criar um registro com o tipo de atestado SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="7f78c-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="7f78c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7f78c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="7f78c-114">Crie um registro com atestado TPM.</span><span class="sxs-lookup"><span data-stu-id="7f78c-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="7f78c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7f78c-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="7f78c-116">Criar um registro com o tipo de atestado X509</span><span class="sxs-lookup"><span data-stu-id="7f78c-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="7f78c-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7f78c-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="7f78c-118">Crie um registro com o tipo de atestado SymmetricKey e o estado de "bitexto inicial".</span><span class="sxs-lookup"><span data-stu-id="7f78c-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="7f78c-119">OS</span><span class="sxs-lookup"><span data-stu-id="7f78c-119">PARAMETERS</span></span>

### <span data-ttu-id="7f78c-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7f78c-120">-AllocationPolicy</span></span>
<span data-ttu-id="7f78c-121">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="7f78c-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7f78c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f78c-122">-ApiVersion</span></span>
<span data-ttu-id="7f78c-123">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="7f78c-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7f78c-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="7f78c-124">-AttestationType</span></span>
<span data-ttu-id="7f78c-125">Mecanismo de atestado.</span><span class="sxs-lookup"><span data-stu-id="7f78c-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="7f78c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f78c-126">-DefaultProfile</span></span>
<span data-ttu-id="7f78c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f78c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f78c-128">-Desejado</span><span class="sxs-lookup"><span data-stu-id="7f78c-128">-Desired</span></span>
<span data-ttu-id="7f78c-129">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="7f78c-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7f78c-130">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="7f78c-130">-DeviceId</span></span>
<span data-ttu-id="7f78c-131">ID do dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="7f78c-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="7f78c-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7f78c-132">-DpsName</span></span>
<span data-ttu-id="7f78c-133">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7f78c-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7f78c-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7f78c-134">-DpsObject</span></span>
<span data-ttu-id="7f78c-135">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7f78c-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7f78c-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7f78c-136">-EdgeEnabled</span></span>
<span data-ttu-id="7f78c-137">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="7f78c-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7f78c-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="7f78c-138">-EndorsementKey</span></span>
<span data-ttu-id="7f78c-139">Chave de endosso TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="7f78c-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="7f78c-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7f78c-140">-IotHub</span></span>
<span data-ttu-id="7f78c-141">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="7f78c-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7f78c-142">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="7f78c-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7f78c-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7f78c-143">-IotHubHostName</span></span>
<span data-ttu-id="7f78c-144">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="7f78c-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7f78c-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="7f78c-145">-PrimaryCAName</span></span>
<span data-ttu-id="7f78c-146">O nome do certificado da CA raiz primária.</span><span class="sxs-lookup"><span data-stu-id="7f78c-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="7f78c-147">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="7f78c-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7f78c-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7f78c-148">-PrimaryCertificate</span></span>
<span data-ttu-id="7f78c-149">O caminho para o arquivo que contém o certificado primário.</span><span class="sxs-lookup"><span data-stu-id="7f78c-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="7f78c-150">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="7f78c-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7f78c-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7f78c-151">-PrimaryKey</span></span>
<span data-ttu-id="7f78c-152">A chave de acesso compartilhado simétrico principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="7f78c-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7f78c-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7f78c-153">-ProvisioningStatus</span></span>
<span data-ttu-id="7f78c-154">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="7f78c-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7f78c-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="7f78c-155">-RegistrationId</span></span>
<span data-ttu-id="7f78c-156">ID de registro de inscrição individual.</span><span class="sxs-lookup"><span data-stu-id="7f78c-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="7f78c-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7f78c-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="7f78c-158">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="7f78c-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7f78c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f78c-159">-ResourceGroupName</span></span>
<span data-ttu-id="7f78c-160">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7f78c-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7f78c-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f78c-161">-ResourceId</span></span>
<span data-ttu-id="7f78c-162">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7f78c-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7f78c-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f78c-163">-RootCertificate</span></span>
<span data-ttu-id="7f78c-164">Permite criar X509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="7f78c-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="7f78c-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="7f78c-165">-SecondaryCAName</span></span>
<span data-ttu-id="7f78c-166">O nome do certificado da autoridade de certificação raiz secundária.</span><span class="sxs-lookup"><span data-stu-id="7f78c-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="7f78c-167">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="7f78c-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7f78c-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7f78c-168">-SecondaryCertificate</span></span>
<span data-ttu-id="7f78c-169">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="7f78c-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="7f78c-170">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="7f78c-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7f78c-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7f78c-171">-SecondaryKey</span></span>
<span data-ttu-id="7f78c-172">A chave de acesso compartilhado simétrico secundário armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="7f78c-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7f78c-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="7f78c-173">-StorageRootKey</span></span>
<span data-ttu-id="7f78c-174">Chave raiz de armazenamento TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="7f78c-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="7f78c-175">-Marca</span><span class="sxs-lookup"><span data-stu-id="7f78c-175">-Tag</span></span>
<span data-ttu-id="7f78c-176">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="7f78c-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="7f78c-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7f78c-177">-WebhookUrl</span></span>
<span data-ttu-id="7f78c-178">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7f78c-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7f78c-179">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f78c-179">-Confirm</span></span>
<span data-ttu-id="7f78c-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f78c-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f78c-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f78c-181">-WhatIf</span></span>
<span data-ttu-id="7f78c-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f78c-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f78c-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f78c-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f78c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f78c-184">CommonParameters</span></span>
<span data-ttu-id="7f78c-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f78c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f78c-186">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f78c-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f78c-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f78c-187">INPUTS</span></span>

### <span data-ttu-id="7f78c-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7f78c-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7f78c-189">System. String</span><span class="sxs-lookup"><span data-stu-id="7f78c-189">System.String</span></span>

## <span data-ttu-id="7f78c-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f78c-190">OUTPUTS</span></span>

### <span data-ttu-id="7f78c-191">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="7f78c-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="7f78c-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f78c-192">NOTES</span></span>

## <span data-ttu-id="7f78c-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f78c-193">RELATED LINKS</span></span>
