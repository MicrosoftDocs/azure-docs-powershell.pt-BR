---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116747"
---
# <span data-ttu-id="1115d-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="1115d-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="1115d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1115d-102">SYNOPSIS</span></span>
<span data-ttu-id="1115d-103">Lista todos os certificados ou um certificado específico contido em um Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1115d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="1115d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1115d-104">SYNTAX</span></span>

### <span data-ttu-id="1115d-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1115d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1115d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1115d-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1115d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1115d-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1115d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1115d-108">DESCRIPTION</span></span>
<span data-ttu-id="1115d-109">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="1115d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="1115d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1115d-110">EXAMPLES</span></span>

### <span data-ttu-id="1115d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1115d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="1115d-112">Listar todos os certificados no MyIotHub</span><span class="sxs-lookup"><span data-stu-id="1115d-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="1115d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1115d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="1115d-114">Mostrar detalhes sobre o MyCertificate</span><span class="sxs-lookup"><span data-stu-id="1115d-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="1115d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1115d-115">PARAMETERS</span></span>

### <span data-ttu-id="1115d-116">-Nomedo Certificado</span><span class="sxs-lookup"><span data-stu-id="1115d-116">-CertificateName</span></span>
<span data-ttu-id="1115d-117">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="1115d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="1115d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1115d-118">-DefaultProfile</span></span>
<span data-ttu-id="1115d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1115d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1115d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1115d-120">-InputObject</span></span>
<span data-ttu-id="1115d-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1115d-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1115d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1115d-122">-Name</span></span>
<span data-ttu-id="1115d-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1115d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1115d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1115d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1115d-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1115d-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1115d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1115d-126">-ResourceId</span></span>
<span data-ttu-id="1115d-127">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="1115d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1115d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1115d-128">CommonParameters</span></span>
<span data-ttu-id="1115d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1115d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1115d-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1115d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1115d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="1115d-131">INPUTS</span></span>

### <span data-ttu-id="1115d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1115d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1115d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1115d-133">System.String</span></span>

## <span data-ttu-id="1115d-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1115d-134">OUTPUTS</span></span>

### <span data-ttu-id="1115d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="1115d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="1115d-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1115d-136">NOTES</span></span>

## <span data-ttu-id="1115d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1115d-137">RELATED LINKS</span></span>
