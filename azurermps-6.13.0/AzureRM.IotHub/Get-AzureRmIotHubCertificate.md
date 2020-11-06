---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 745fcb6fdfb9ee47faf28cde84985dcfd7199ecc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440418"
---
# <span data-ttu-id="c0ae9-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="c0ae9-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="c0ae9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ae9-103">Lista todos os certificados ou um determinado certificado contido em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ae9-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ae9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0ae9-104">SYNTAX</span></span>

### <span data-ttu-id="c0ae9-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0ae9-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ae9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0ae9-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ae9-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c0ae9-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ae9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="c0ae9-109">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c0ae9-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c0ae9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0ae9-110">EXAMPLES</span></span>

### <span data-ttu-id="c0ae9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0ae9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="c0ae9-112">Listar todos os certificados no MyIotHub</span><span class="sxs-lookup"><span data-stu-id="c0ae9-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="c0ae9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0ae9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="c0ae9-114">Mostrar detalhes sobre mycertification</span><span class="sxs-lookup"><span data-stu-id="c0ae9-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="c0ae9-115">OS</span><span class="sxs-lookup"><span data-stu-id="c0ae9-115">PARAMETERS</span></span>

### <span data-ttu-id="c0ae9-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c0ae9-116">-CertificateName</span></span>
<span data-ttu-id="c0ae9-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="c0ae9-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c0ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="c0ae9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ae9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ae9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0ae9-120">-InputObject</span></span>
<span data-ttu-id="c0ae9-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="c0ae9-121">IotHub Object</span></span>

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

### <span data-ttu-id="c0ae9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0ae9-122">-Name</span></span>
<span data-ttu-id="c0ae9-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="c0ae9-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c0ae9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ae9-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0ae9-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c0ae9-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0ae9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ae9-126">-ResourceId</span></span>
<span data-ttu-id="c0ae9-127">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="c0ae9-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c0ae9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ae9-128">CommonParameters</span></span>
<span data-ttu-id="c0ae9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ae9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ae9-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ae9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ae9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0ae9-131">INPUTS</span></span>

### <span data-ttu-id="c0ae9-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c0ae9-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="c0ae9-133">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0ae9-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c0ae9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0ae9-134">System.String</span></span>

## <span data-ttu-id="c0ae9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0ae9-135">OUTPUTS</span></span>

### <span data-ttu-id="c0ae9-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c0ae9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="c0ae9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0ae9-137">NOTES</span></span>

## <span data-ttu-id="c0ae9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0ae9-138">RELATED LINKS</span></span>
