---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117448"
---
# <span data-ttu-id="037e7-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="037e7-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="037e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="037e7-102">SYNOPSIS</span></span>
<span data-ttu-id="037e7-103">Obtém a lista de recursos de informações de marca de serviço.</span><span class="sxs-lookup"><span data-stu-id="037e7-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="037e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="037e7-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="037e7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="037e7-105">DESCRIPTION</span></span>
<span data-ttu-id="037e7-106">O **cmdlet Get-AzNetworkServiceTag** obtém a lista de recursos de informações de marca de serviço.</span><span class="sxs-lookup"><span data-stu-id="037e7-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="037e7-107">Observe que as informações da região do Azure especificadas serão usadas como referência para a versão (não como um filtro com base no local).</span><span class="sxs-lookup"><span data-stu-id="037e7-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="037e7-108">Por exemplo, mesmo que você especifique, receberá a lista de marcas de serviço com detalhes de prefixo em todas as regiões, mas limitado à nuvem à qual sua assinatura `-Location eastus2` pertence (ou seja, Pública, governo dos EUA, China ou Alemanha).</span><span class="sxs-lookup"><span data-stu-id="037e7-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="037e7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="037e7-109">EXAMPLES</span></span>

### <span data-ttu-id="037e7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="037e7-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="037e7-111">O comando obtém a lista de recursos de informações de marca de serviço e o armazena em `serviceTags` variável.</span><span class="sxs-lookup"><span data-stu-id="037e7-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="037e7-112">Exemplo 2: Obter todos os prefixos de endereço do AzureSQL</span><span class="sxs-lookup"><span data-stu-id="037e7-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="037e7-113">O primeiro comando obtém a lista de recursos de informações de marca de serviço e o armazena em `serviceTags` variável.</span><span class="sxs-lookup"><span data-stu-id="037e7-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="037e7-114">O segundo comando filtra a lista para selecionar o recurso de informações do Sql.</span><span class="sxs-lookup"><span data-stu-id="037e7-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="037e7-115">Exemplo 3: Obter o recurso de informações de marca de serviço do Armazenamento para o West US 2</span><span class="sxs-lookup"><span data-stu-id="037e7-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="037e7-116">O primeiro comando obtém a lista de recursos de informações de marca de serviço e o armazena em `serviceTags` variável.</span><span class="sxs-lookup"><span data-stu-id="037e7-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="037e7-117">Os comandos a seguir mostram várias maneiras de filtrar a lista para selecionar informações de marca de serviço para Armazenamento no Oeste dos EUA 2.</span><span class="sxs-lookup"><span data-stu-id="037e7-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="037e7-118">Exemplo 4: Obter todos os recursos de informações de marca de serviço global</span><span class="sxs-lookup"><span data-stu-id="037e7-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="037e7-119">O primeiro comando obtém a lista de recursos de informações de marca de serviço e o armazena em `serviceTags` variável.</span><span class="sxs-lookup"><span data-stu-id="037e7-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="037e7-120">O segundo comando filtra a lista para selecionar somente aqueles sem definir região.</span><span class="sxs-lookup"><span data-stu-id="037e7-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="037e7-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="037e7-121">PARAMETERS</span></span>

### <span data-ttu-id="037e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037e7-122">-DefaultProfile</span></span>
<span data-ttu-id="037e7-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="037e7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="037e7-124">-Local</span><span class="sxs-lookup"><span data-stu-id="037e7-124">-Location</span></span>
<span data-ttu-id="037e7-125">O local que será usado como referência para a versão (não como um filtro com base na localização, você receberá a lista de marcas de serviço com detalhes de prefixo em todas as regiões, mas limitado à nuvem à onde sua assinatura pertence).</span><span class="sxs-lookup"><span data-stu-id="037e7-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037e7-126">CommonParameters</span></span>
<span data-ttu-id="037e7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037e7-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="037e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037e7-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="037e7-129">INPUTS</span></span>

### <span data-ttu-id="037e7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="037e7-130">System.String</span></span>

## <span data-ttu-id="037e7-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="037e7-131">OUTPUTS</span></span>

### <span data-ttu-id="037e7-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="037e7-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="037e7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="037e7-133">NOTES</span></span>

## <span data-ttu-id="037e7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="037e7-134">RELATED LINKS</span></span>
