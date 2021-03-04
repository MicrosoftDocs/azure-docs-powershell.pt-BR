---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 89a1bede6ff90b58b83a7c401860c66430958fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891192"
---
# <span data-ttu-id="2616c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="2616c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="2616c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2616c-102">SYNOPSIS</span></span>
<span data-ttu-id="2616c-103">Criar um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2616c-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="2616c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2616c-104">SYNTAX</span></span>

### <span data-ttu-id="2616c-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2616c-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2616c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2616c-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2616c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2616c-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2616c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2616c-108">DESCRIPTION</span></span>
<span data-ttu-id="2616c-109">Crie um grupo de registro em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="2616c-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2616c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2616c-110">EXAMPLES</span></span>

### <span data-ttu-id="2616c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2616c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="2616c-112">Criar um registro com o tipo de atestado SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="2616c-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="2616c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2616c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="2616c-114">Criar um registro com o tipo de atestado X509</span><span class="sxs-lookup"><span data-stu-id="2616c-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="2616c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2616c-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="2616c-116">Crie um registro com o tipo de atestado SymmetricKey e estado duplo inicial.</span><span class="sxs-lookup"><span data-stu-id="2616c-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="2616c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2616c-117">PARAMETERS</span></span>

### <span data-ttu-id="2616c-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2616c-118">-AllocationPolicy</span></span>
<span data-ttu-id="2616c-119">Tipo de alocação para dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="2616c-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="2616c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2616c-120">-ApiVersion</span></span>
<span data-ttu-id="2616c-121">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="2616c-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="2616c-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="2616c-122">-AttestationType</span></span>
<span data-ttu-id="2616c-123">Mecanismo de atestado.</span><span class="sxs-lookup"><span data-stu-id="2616c-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="2616c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2616c-124">-DefaultProfile</span></span>
<span data-ttu-id="2616c-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2616c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2616c-126">-Desired</span><span class="sxs-lookup"><span data-stu-id="2616c-126">-Desired</span></span>
<span data-ttu-id="2616c-127">Propriedades iniciais desejadas para o irmão duplo.</span><span class="sxs-lookup"><span data-stu-id="2616c-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="2616c-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2616c-128">-DpsName</span></span>
<span data-ttu-id="2616c-129">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="2616c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2616c-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2616c-130">-DpsObject</span></span>
<span data-ttu-id="2616c-131">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2616c-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2616c-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2616c-132">-EdgeEnabled</span></span>
<span data-ttu-id="2616c-133">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="2616c-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="2616c-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="2616c-134">-IotHub</span></span>
<span data-ttu-id="2616c-135">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="2616c-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="2616c-136">Use a lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="2616c-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="2616c-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="2616c-137">-IotHubHostName</span></span>
<span data-ttu-id="2616c-138">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="2616c-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="2616c-139">-Name</span><span class="sxs-lookup"><span data-stu-id="2616c-139">-Name</span></span>
<span data-ttu-id="2616c-140">Nome do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="2616c-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="2616c-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="2616c-141">-PrimaryCAName</span></span>
<span data-ttu-id="2616c-142">O nome do certificado ca raiz principal.</span><span class="sxs-lookup"><span data-stu-id="2616c-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="2616c-143">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="2616c-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="2616c-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="2616c-144">-PrimaryCertificate</span></span>
<span data-ttu-id="2616c-145">O caminho para o arquivo que contém o certificado principal.</span><span class="sxs-lookup"><span data-stu-id="2616c-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="2616c-146">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="2616c-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="2616c-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2616c-147">-PrimaryKey</span></span>
<span data-ttu-id="2616c-148">A chave de acesso compartilhado simétrica principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="2616c-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="2616c-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="2616c-149">-ProvisioningStatus</span></span>
<span data-ttu-id="2616c-150">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="2616c-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="2616c-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="2616c-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="2616c-152">Dados do dispositivo a serem tratados na re provisionamento para hub de Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="2616c-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="2616c-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2616c-153">-ResourceGroupName</span></span>
<span data-ttu-id="2616c-154">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2616c-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2616c-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2616c-155">-ResourceId</span></span>
<span data-ttu-id="2616c-156">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="2616c-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2616c-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="2616c-157">-RootCertificate</span></span>
<span data-ttu-id="2616c-158">Permite criar x509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="2616c-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="2616c-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="2616c-159">-SecondaryCAName</span></span>
<span data-ttu-id="2616c-160">O nome do certificado ca raiz secundário.</span><span class="sxs-lookup"><span data-stu-id="2616c-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="2616c-161">Se o atestado com um certificado ca raiz for desejado, um nome de ca raiz deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="2616c-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="2616c-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="2616c-162">-SecondaryCertificate</span></span>
<span data-ttu-id="2616c-163">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="2616c-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="2616c-164">Representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="2616c-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="2616c-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="2616c-165">-SecondaryKey</span></span>
<span data-ttu-id="2616c-166">A chave de acesso compartilhado simétrica secundária armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="2616c-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="2616c-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="2616c-167">-Tag</span></span>
<span data-ttu-id="2616c-168">Marcas duplas iniciais.</span><span class="sxs-lookup"><span data-stu-id="2616c-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="2616c-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="2616c-169">-WebhookUrl</span></span>
<span data-ttu-id="2616c-170">A URL de webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2616c-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="2616c-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2616c-171">-Confirm</span></span>
<span data-ttu-id="2616c-172">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2616c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2616c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2616c-173">-WhatIf</span></span>
<span data-ttu-id="2616c-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2616c-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2616c-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2616c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2616c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2616c-176">CommonParameters</span></span>
<span data-ttu-id="2616c-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2616c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2616c-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2616c-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2616c-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2616c-179">INPUTS</span></span>

### <span data-ttu-id="2616c-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2616c-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2616c-181">System.String</span><span class="sxs-lookup"><span data-stu-id="2616c-181">System.String</span></span>

## <span data-ttu-id="2616c-182">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2616c-182">OUTPUTS</span></span>

### <span data-ttu-id="2616c-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="2616c-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="2616c-184">NOTES</span><span class="sxs-lookup"><span data-stu-id="2616c-184">NOTES</span></span>

## <span data-ttu-id="2616c-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2616c-185">RELATED LINKS</span></span>
