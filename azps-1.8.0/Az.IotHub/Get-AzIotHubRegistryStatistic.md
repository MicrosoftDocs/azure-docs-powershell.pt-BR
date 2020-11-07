---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: bb4ab11406a644d34bdb5b45ea3b3fba47376826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770719"
---
# <span data-ttu-id="fba42-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="fba42-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="fba42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fba42-102">SYNOPSIS</span></span>
<span data-ttu-id="fba42-103">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="fba42-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="fba42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fba42-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba42-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fba42-105">DESCRIPTION</span></span>
<span data-ttu-id="fba42-106">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="fba42-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="fba42-107">Isso fornece informações sobre o número total de dispositivos habilitados, habilitados e desativados em um IotHub.</span><span class="sxs-lookup"><span data-stu-id="fba42-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="fba42-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fba42-108">EXAMPLES</span></span>

### <span data-ttu-id="fba42-109">Exemplo 1 obter o RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="fba42-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fba42-110">Obtém o RegistryStatictics para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fba42-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fba42-111">OS</span><span class="sxs-lookup"><span data-stu-id="fba42-111">PARAMETERS</span></span>

### <span data-ttu-id="fba42-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba42-112">-DefaultProfile</span></span>
<span data-ttu-id="fba42-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fba42-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fba42-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fba42-114">-Name</span></span>
<span data-ttu-id="fba42-115">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fba42-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="fba42-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba42-116">-ResourceGroupName</span></span>
<span data-ttu-id="fba42-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fba42-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fba42-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba42-118">CommonParameters</span></span>
<span data-ttu-id="fba42-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba42-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba42-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba42-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba42-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fba42-121">INPUTS</span></span>

### <span data-ttu-id="fba42-122">System. String</span><span class="sxs-lookup"><span data-stu-id="fba42-122">System.String</span></span>

## <span data-ttu-id="fba42-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fba42-123">OUTPUTS</span></span>

### <span data-ttu-id="fba42-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="fba42-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="fba42-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fba42-125">NOTES</span></span>

## <span data-ttu-id="fba42-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fba42-126">RELATED LINKS</span></span>
