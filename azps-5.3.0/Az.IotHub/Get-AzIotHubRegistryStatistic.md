---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433634"
---
# <span data-ttu-id="9084a-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="9084a-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="9084a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9084a-102">SYNOPSIS</span></span>
<span data-ttu-id="9084a-103">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9084a-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="9084a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9084a-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9084a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9084a-105">DESCRIPTION</span></span>
<span data-ttu-id="9084a-106">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9084a-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="9084a-107">Isso fornece informações sobre o número total de dispositivos habilitados, habilitados e desativados em um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9084a-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="9084a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9084a-108">EXAMPLES</span></span>

### <span data-ttu-id="9084a-109">Exemplo 1 obter o RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="9084a-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9084a-110">Obtém o RegistryStatistics para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="9084a-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9084a-111">OS</span><span class="sxs-lookup"><span data-stu-id="9084a-111">PARAMETERS</span></span>

### <span data-ttu-id="9084a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9084a-112">-DefaultProfile</span></span>
<span data-ttu-id="9084a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9084a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9084a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9084a-114">-Name</span></span>
<span data-ttu-id="9084a-115">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9084a-115">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9084a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9084a-116">-ResourceGroupName</span></span>
<span data-ttu-id="9084a-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9084a-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9084a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9084a-118">CommonParameters</span></span>
<span data-ttu-id="9084a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9084a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9084a-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9084a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9084a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9084a-121">INPUTS</span></span>

### <span data-ttu-id="9084a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9084a-122">System.String</span></span>

## <span data-ttu-id="9084a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9084a-123">OUTPUTS</span></span>

### <span data-ttu-id="9084a-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="9084a-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="9084a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9084a-125">NOTES</span></span>

## <span data-ttu-id="9084a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9084a-126">RELATED LINKS</span></span>
