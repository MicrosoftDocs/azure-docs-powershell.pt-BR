---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115819"
---
# <span data-ttu-id="089f0-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="089f0-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="089f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="089f0-102">SYNOPSIS</span></span>
<span data-ttu-id="089f0-103">Criar um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="089f0-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="089f0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="089f0-104">SYNTAX</span></span>

### <span data-ttu-id="089f0-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="089f0-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="089f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="089f0-106">InputObjectSet</span></span>
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

### <span data-ttu-id="089f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="089f0-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="089f0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="089f0-108">DESCRIPTION</span></span>
<span data-ttu-id="089f0-109">Crie um registro de dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="089f0-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="089f0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="089f0-110">EXAMPLES</span></span>

### <span data-ttu-id="089f0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="089f0-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="089f0-112">Criar um registro com o tipo de teste SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="089f0-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="089f0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="089f0-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="089f0-114">Crie um registro com o teste de TPM.</span><span class="sxs-lookup"><span data-stu-id="089f0-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="089f0-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="089f0-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="089f0-116">Criar um registro com o tipo de teste X509</span><span class="sxs-lookup"><span data-stu-id="089f0-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="089f0-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="089f0-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="089f0-118">Crie um registro com o tipo de teste SymmetricKey e o estado inicial do brilho.</span><span class="sxs-lookup"><span data-stu-id="089f0-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="089f0-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="089f0-119">PARAMETERS</span></span>

### <span data-ttu-id="089f0-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="089f0-120">-AllocationPolicy</span></span>
<span data-ttu-id="089f0-121">Tipo de alocação do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="089f0-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="089f0-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="089f0-122">-ApiVersion</span></span>
<span data-ttu-id="089f0-123">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="089f0-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="089f0-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="089f0-124">-AttestationType</span></span>
<span data-ttu-id="089f0-125">Mecanismo de Teste.</span><span class="sxs-lookup"><span data-stu-id="089f0-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="089f0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089f0-126">-DefaultProfile</span></span>
<span data-ttu-id="089f0-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="089f0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089f0-128">-Desejado</span><span class="sxs-lookup"><span data-stu-id="089f0-128">-Desired</span></span>
<span data-ttu-id="089f0-129">Propriedades iniciais desejadas.</span><span class="sxs-lookup"><span data-stu-id="089f0-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="089f0-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="089f0-130">-DeviceId</span></span>
<span data-ttu-id="089f0-131">ID do dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="089f0-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="089f0-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="089f0-132">-DpsName</span></span>
<span data-ttu-id="089f0-133">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="089f0-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="089f0-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="089f0-134">-DpsObject</span></span>
<span data-ttu-id="089f0-135">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="089f0-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="089f0-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="089f0-136">-EdgeEnabled</span></span>
<span data-ttu-id="089f0-137">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="089f0-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="089f0-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="089f0-138">-EndorsementKey</span></span>
<span data-ttu-id="089f0-139">Chave de endosso de TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="089f0-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="089f0-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="089f0-140">-IotHub</span></span>
<span data-ttu-id="089f0-141">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="089f0-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="089f0-142">Use uma lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="089f0-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="089f0-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="089f0-143">-IotHubHostName</span></span>
<span data-ttu-id="089f0-144">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="089f0-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="089f0-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="089f0-145">-PrimaryCAName</span></span>
<span data-ttu-id="089f0-146">O nome do certificado de AC raiz principal.</span><span class="sxs-lookup"><span data-stu-id="089f0-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="089f0-147">Se o teste com um certificado de AC raiz for desejado, um nome de ca raiz deverá ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="089f0-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="089f0-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="089f0-148">-PrimaryCertificate</span></span>
<span data-ttu-id="089f0-149">O caminho para o arquivo que contém o certificado principal.</span><span class="sxs-lookup"><span data-stu-id="089f0-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="089f0-150">Representação de base 64 do arquivo .cer de certificado X509 ou do caminho de arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="089f0-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="089f0-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="089f0-151">-PrimaryKey</span></span>
<span data-ttu-id="089f0-152">A chave de acesso compartilhado simétrica principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="089f0-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="089f0-153">-ProvisionandoStatus</span><span class="sxs-lookup"><span data-stu-id="089f0-153">-ProvisioningStatus</span></span>
<span data-ttu-id="089f0-154">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="089f0-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="089f0-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="089f0-155">-RegistrationId</span></span>
<span data-ttu-id="089f0-156">ID do registro individual.</span><span class="sxs-lookup"><span data-stu-id="089f0-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="089f0-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="089f0-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="089f0-158">Dados do dispositivo a serem tratados na provisionamento de novo para o Hub Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="089f0-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="089f0-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089f0-159">-ResourceGroupName</span></span>
<span data-ttu-id="089f0-160">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="089f0-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="089f0-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="089f0-161">-ResourceId</span></span>
<span data-ttu-id="089f0-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="089f0-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="089f0-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="089f0-163">-RootCertificate</span></span>
<span data-ttu-id="089f0-164">Permite criar estações X509atte usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="089f0-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="089f0-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="089f0-165">-SecondaryCAName</span></span>
<span data-ttu-id="089f0-166">O nome do certificado de AC raiz secundário.</span><span class="sxs-lookup"><span data-stu-id="089f0-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="089f0-167">Se o teste com um certificado de AC raiz for desejado, um nome de ca raiz deverá ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="089f0-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="089f0-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="089f0-168">-SecondaryCertificate</span></span>
<span data-ttu-id="089f0-169">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="089f0-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="089f0-170">Representação de base 64 do arquivo .cer de certificado X509 ou do caminho de arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="089f0-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="089f0-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="089f0-171">-SecondaryKey</span></span>
<span data-ttu-id="089f0-172">A chave de acesso compartilhado simétrica secundária armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="089f0-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="089f0-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="089f0-173">-StorageRootKey</span></span>
<span data-ttu-id="089f0-174">Chave raiz de armazenamento TPM para um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="089f0-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="089f0-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="089f0-175">-Tag</span></span>
<span data-ttu-id="089f0-176">Marcas iniciais de brilho.</span><span class="sxs-lookup"><span data-stu-id="089f0-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="089f0-177">-WebçãoUrl</span><span class="sxs-lookup"><span data-stu-id="089f0-177">-WebhookUrl</span></span>
<span data-ttu-id="089f0-178">A URL web url usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="089f0-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="089f0-179">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="089f0-179">-Confirm</span></span>
<span data-ttu-id="089f0-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="089f0-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089f0-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089f0-181">-WhatIf</span></span>
<span data-ttu-id="089f0-182">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="089f0-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="089f0-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="089f0-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="089f0-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089f0-184">CommonParameters</span></span>
<span data-ttu-id="089f0-185">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089f0-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089f0-186">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089f0-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089f0-187">Entradas</span><span class="sxs-lookup"><span data-stu-id="089f0-187">INPUTS</span></span>

### <span data-ttu-id="089f0-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="089f0-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="089f0-189">System.String</span><span class="sxs-lookup"><span data-stu-id="089f0-189">System.String</span></span>

## <span data-ttu-id="089f0-190">Saídas</span><span class="sxs-lookup"><span data-stu-id="089f0-190">OUTPUTS</span></span>

### <span data-ttu-id="089f0-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="089f0-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="089f0-192">Notas</span><span class="sxs-lookup"><span data-stu-id="089f0-192">NOTES</span></span>

## <span data-ttu-id="089f0-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="089f0-193">RELATED LINKS</span></span>
