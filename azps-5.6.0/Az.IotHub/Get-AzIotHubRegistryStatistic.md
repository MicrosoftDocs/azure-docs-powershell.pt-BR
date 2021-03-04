---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 251692538dbd9c5db28718c5833c9a3d096d9503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889935"
---
# <span data-ttu-id="7e5ce-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="7e5ce-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="7e5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5ce-103">Obtém o RegistryStatistics para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e5ce-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="7e5ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e5ce-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e5ce-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="7e5ce-106">Obtém o RegistryStatistics para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e5ce-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="7e5ce-107">Isso fornece informações sobre o número total de dispositivos habilitados e desabilitados em um IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e5ce-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="7e5ce-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-108">EXAMPLES</span></span>

### <span data-ttu-id="7e5ce-109">Exemplo 1 Obter o RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="7e5ce-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7e5ce-110">Obtém o RegistryStatistics do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7e5ce-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7e5ce-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-111">PARAMETERS</span></span>

### <span data-ttu-id="7e5ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5ce-112">-DefaultProfile</span></span>
<span data-ttu-id="7e5ce-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7e5ce-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e5ce-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7e5ce-114">-Name</span></span>
<span data-ttu-id="7e5ce-115">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="7e5ce-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7e5ce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5ce-116">-ResourceGroupName</span></span>
<span data-ttu-id="7e5ce-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7e5ce-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7e5ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5ce-118">CommonParameters</span></span>
<span data-ttu-id="7e5ce-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5ce-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e5ce-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5ce-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-121">INPUTS</span></span>

### <span data-ttu-id="7e5ce-122">System.String</span><span class="sxs-lookup"><span data-stu-id="7e5ce-122">System.String</span></span>

## <span data-ttu-id="7e5ce-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-123">OUTPUTS</span></span>

### <span data-ttu-id="7e5ce-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="7e5ce-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="7e5ce-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e5ce-125">NOTES</span></span>

## <span data-ttu-id="7e5ce-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e5ce-126">RELATED LINKS</span></span>
