---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948304"
---
# <span data-ttu-id="5b890-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="5b890-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="5b890-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b890-102">SYNOPSIS</span></span>
<span data-ttu-id="5b890-103">Crie um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b890-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="5b890-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b890-104">SYNTAX</span></span>

### <span data-ttu-id="5b890-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b890-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b890-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b890-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b890-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5b890-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b890-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b890-108">DESCRIPTION</span></span>
<span data-ttu-id="5b890-109">Crie um grupo de inscrição em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="5b890-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5b890-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b890-110">EXAMPLES</span></span>

### <span data-ttu-id="5b890-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b890-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="5b890-112">Criar um registro com o tipo de atestado SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="5b890-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="5b890-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5b890-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="5b890-114">Criar um registro com o tipo de atestado X509</span><span class="sxs-lookup"><span data-stu-id="5b890-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="5b890-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5b890-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="5b890-116">Crie um registro com o tipo de atestado SymmetricKey e o estado de "bitexto inicial".</span><span class="sxs-lookup"><span data-stu-id="5b890-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="5b890-117">OS</span><span class="sxs-lookup"><span data-stu-id="5b890-117">PARAMETERS</span></span>

### <span data-ttu-id="5b890-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5b890-118">-AllocationPolicy</span></span>
<span data-ttu-id="5b890-119">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="5b890-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="5b890-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b890-120">-ApiVersion</span></span>
<span data-ttu-id="5b890-121">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="5b890-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="5b890-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="5b890-122">-AttestationType</span></span>
<span data-ttu-id="5b890-123">Mecanismo de atestado.</span><span class="sxs-lookup"><span data-stu-id="5b890-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="5b890-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b890-124">-DefaultProfile</span></span>
<span data-ttu-id="5b890-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b890-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b890-126">-Desejado</span><span class="sxs-lookup"><span data-stu-id="5b890-126">-Desired</span></span>
<span data-ttu-id="5b890-127">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="5b890-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="5b890-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5b890-128">-DpsName</span></span>
<span data-ttu-id="5b890-129">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5b890-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5b890-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5b890-130">-DpsObject</span></span>
<span data-ttu-id="5b890-131">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5b890-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5b890-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5b890-132">-EdgeEnabled</span></span>
<span data-ttu-id="5b890-133">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="5b890-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="5b890-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="5b890-134">-IotHub</span></span>
<span data-ttu-id="5b890-135">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="5b890-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="5b890-136">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="5b890-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="5b890-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="5b890-137">-IotHubHostName</span></span>
<span data-ttu-id="5b890-138">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="5b890-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="5b890-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b890-139">-Name</span></span>
<span data-ttu-id="5b890-140">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="5b890-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="5b890-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="5b890-141">-PrimaryCAName</span></span>
<span data-ttu-id="5b890-142">O nome do certificado da CA raiz primária.</span><span class="sxs-lookup"><span data-stu-id="5b890-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="5b890-143">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="5b890-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="5b890-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="5b890-144">-PrimaryCertificate</span></span>
<span data-ttu-id="5b890-145">O caminho para o arquivo que contém o certificado primário.</span><span class="sxs-lookup"><span data-stu-id="5b890-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="5b890-146">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="5b890-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="5b890-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5b890-147">-PrimaryKey</span></span>
<span data-ttu-id="5b890-148">A chave de acesso compartilhado simétrico principal armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="5b890-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="5b890-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="5b890-149">-ProvisioningStatus</span></span>
<span data-ttu-id="5b890-150">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="5b890-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="5b890-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="5b890-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="5b890-152">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="5b890-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="5b890-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b890-153">-ResourceGroupName</span></span>
<span data-ttu-id="5b890-154">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5b890-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b890-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b890-155">-ResourceId</span></span>
<span data-ttu-id="5b890-156">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5b890-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5b890-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="5b890-157">-RootCertificate</span></span>
<span data-ttu-id="5b890-158">Permite criar X509attestation usando certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="5b890-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="5b890-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="5b890-159">-SecondaryCAName</span></span>
<span data-ttu-id="5b890-160">O nome do certificado da autoridade de certificação raiz secundária.</span><span class="sxs-lookup"><span data-stu-id="5b890-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="5b890-161">Se o atestado com um certificado de CA raiz for necessário, será necessário fornecer um nome de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="5b890-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="5b890-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="5b890-162">-SecondaryCertificate</span></span>
<span data-ttu-id="5b890-163">O caminho para o arquivo que contém o certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="5b890-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="5b890-164">Base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="5b890-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="5b890-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5b890-165">-SecondaryKey</span></span>
<span data-ttu-id="5b890-166">A chave de acesso compartilhado simétrico secundário armazenada no formato base64.</span><span class="sxs-lookup"><span data-stu-id="5b890-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="5b890-167">-Marca</span><span class="sxs-lookup"><span data-stu-id="5b890-167">-Tag</span></span>
<span data-ttu-id="5b890-168">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="5b890-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="5b890-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="5b890-169">-WebhookUrl</span></span>
<span data-ttu-id="5b890-170">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5b890-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="5b890-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b890-171">-Confirm</span></span>
<span data-ttu-id="5b890-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b890-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b890-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b890-173">-WhatIf</span></span>
<span data-ttu-id="5b890-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b890-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b890-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b890-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b890-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b890-176">CommonParameters</span></span>
<span data-ttu-id="5b890-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b890-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b890-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b890-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b890-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b890-179">INPUTS</span></span>

### <span data-ttu-id="5b890-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5b890-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5b890-181">System. String</span><span class="sxs-lookup"><span data-stu-id="5b890-181">System.String</span></span>

## <span data-ttu-id="5b890-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b890-182">OUTPUTS</span></span>

### <span data-ttu-id="5b890-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="5b890-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="5b890-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b890-184">NOTES</span></span>

## <span data-ttu-id="5b890-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b890-185">RELATED LINKS</span></span>
