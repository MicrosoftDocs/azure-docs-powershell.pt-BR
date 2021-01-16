---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428385"
---
# <span data-ttu-id="6757f-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6757f-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="6757f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6757f-102">SYNOPSIS</span></span>
<span data-ttu-id="6757f-103">Crie um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6757f-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="6757f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6757f-104">SYNTAX</span></span>

### <span data-ttu-id="6757f-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6757f-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6757f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6757f-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6757f-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6757f-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6757f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6757f-108">DESCRIPTION</span></span>
<span data-ttu-id="6757f-109">Crie um grupo de inscrição em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="6757f-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6757f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6757f-110">EXAMPLES</span></span>

### <span data-ttu-id="6757f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6757f-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="6757f-112">Criar um registro com o tipo de atestado SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="6757f-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="6757f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6757f-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="6757f-114">Criar um registro com o tipo de atestado X509</span><span class="sxs-lookup"><span data-stu-id="6757f-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="6757f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6757f-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="6757f-116">Crie um registro com o tipo de atestado SymmetricKey e o estado de "bitexto inicial".</span><span class="sxs-lookup"><span data-stu-id="6757f-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="6757f-117">OS</span><span class="sxs-lookup"><span data-stu-id="6757f-117">PARAMETERS</span></span>

### <span data-ttu-id="6757f-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="6757f-118">-AllocationPolicy</span></span>
<span data-ttu-id="6757f-119">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="6757f-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="6757f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6757f-120">-ApiVersion</span></span>
<span data-ttu-id="6757f-121">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="6757f-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="6757f-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="6757f-122">-AttestationType</span></span>
<span data-ttu-id="6757f-123">Mecanismo de atestado.</span><span class="sxs-lookup"><span data-stu-id="6757f-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="6757f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6757f-124">-DefaultProfile</span></span>
<span data-ttu-id="6757f-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6757f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6757f-126">-Desejado</span><span class="sxs-lookup"><span data-stu-id="6757f-126">-Desired</span></span>
<span data-ttu-id="6757f-127">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="6757f-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="6757f-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6757f-128">-DpsName</span></span>
<span data-ttu-id="6757f-129">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6757f-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6757f-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6757f-130">-DpsObject</span></span>
<span data-ttu-id="6757f-131">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6757f-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6757f-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6757f-132">-EdgeEnabled</span></span>
<span data-ttu-id="6757f-133">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="6757f-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6757f-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="6757f-134">-IotHub</span></span>
<span data-ttu-id="6757f-135">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="6757f-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="6757f-136">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="6757f-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="6757f-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="6757f-137">-IotHubHostName</span></span>
<span data-ttu-id="6757f-138">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="6757f-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="6757f-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="6757f-139">-Name</span></span>
<span data-ttu-id="6757f-140">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="6757f-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="6757f-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="6757f-141">-PrimaryCAName</span></span>
<span data-ttu-id="6757f-142">O nome do certificado da CA raiz primária.</span><span class="sxs-lookup"><span data-stu-id="6757f-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="6757f-143">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="6757f-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="6757f-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="6757f-144">-PrimaryCertificate</span></span>
<span data-ttu-id="6757f-145">O caminho para o arquivo que contém o certificado primário.</span><span class="sxs-lookup"><span data-stu-id="6757f-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="6757f-146">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="6757f-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="6757f-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="6757f-147">-PrimaryKey</span></span>
<span data-ttu-id="6757f-148">A chave de acesso compartilhado simétrico principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="6757f-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="6757f-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="6757f-149">-ProvisioningStatus</span></span>
<span data-ttu-id="6757f-150">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="6757f-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="6757f-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="6757f-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="6757f-152">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="6757f-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="6757f-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6757f-153">-ResourceGroupName</span></span>
<span data-ttu-id="6757f-154">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6757f-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6757f-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6757f-155">-ResourceId</span></span>
<span data-ttu-id="6757f-156">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6757f-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6757f-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="6757f-157">-RootCertificate</span></span>
<span data-ttu-id="6757f-158">Permite criar X509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="6757f-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="6757f-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="6757f-159">-SecondaryCAName</span></span>
<span data-ttu-id="6757f-160">O nome do certificado da autoridade de certificação raiz secundária.</span><span class="sxs-lookup"><span data-stu-id="6757f-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="6757f-161">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="6757f-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="6757f-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="6757f-162">-SecondaryCertificate</span></span>
<span data-ttu-id="6757f-163">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="6757f-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="6757f-164">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="6757f-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="6757f-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="6757f-165">-SecondaryKey</span></span>
<span data-ttu-id="6757f-166">A chave de acesso compartilhado simétrico secundário armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="6757f-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="6757f-167">-Marca</span><span class="sxs-lookup"><span data-stu-id="6757f-167">-Tag</span></span>
<span data-ttu-id="6757f-168">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="6757f-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="6757f-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="6757f-169">-WebhookUrl</span></span>
<span data-ttu-id="6757f-170">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6757f-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="6757f-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6757f-171">-Confirm</span></span>
<span data-ttu-id="6757f-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6757f-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6757f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6757f-173">-WhatIf</span></span>
<span data-ttu-id="6757f-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6757f-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6757f-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6757f-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6757f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6757f-176">CommonParameters</span></span>
<span data-ttu-id="6757f-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6757f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6757f-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6757f-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6757f-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6757f-179">INPUTS</span></span>

### <span data-ttu-id="6757f-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6757f-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6757f-181">System. String</span><span class="sxs-lookup"><span data-stu-id="6757f-181">System.String</span></span>

## <span data-ttu-id="6757f-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6757f-182">OUTPUTS</span></span>

### <span data-ttu-id="6757f-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6757f-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="6757f-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6757f-184">NOTES</span></span>

## <span data-ttu-id="6757f-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6757f-185">RELATED LINKS</span></span>
