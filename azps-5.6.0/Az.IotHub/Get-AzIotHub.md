---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889975"
---
# <span data-ttu-id="37fa1-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="37fa1-101">Get-AzIotHub</span></span>

## <span data-ttu-id="37fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="37fa1-103">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="37fa1-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="37fa1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37fa1-104">SYNTAX</span></span>

### <span data-ttu-id="37fa1-105">ListIotHubsByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37fa1-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37fa1-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="37fa1-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37fa1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37fa1-107">DESCRIPTION</span></span>
<span data-ttu-id="37fa1-108">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="37fa1-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="37fa1-109">Você pode exibir todas as instâncias do IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome IotHub específico.</span><span class="sxs-lookup"><span data-stu-id="37fa1-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="37fa1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37fa1-110">EXAMPLES</span></span>

### <span data-ttu-id="37fa1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37fa1-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="37fa1-112">Obtém todos os IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="37fa1-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="37fa1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37fa1-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="37fa1-114">Obtém todos os IotHubs na assinatura pertencente ao grupo de recursos chamado "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="37fa1-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="37fa1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="37fa1-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="37fa1-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="37fa1-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="37fa1-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37fa1-117">PARAMETERS</span></span>

### <span data-ttu-id="37fa1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fa1-118">-DefaultProfile</span></span>
<span data-ttu-id="37fa1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="37fa1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37fa1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="37fa1-120">-Name</span></span>
<span data-ttu-id="37fa1-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="37fa1-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="37fa1-123">Nome do ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37fa1-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fa1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fa1-124">CommonParameters</span></span>
<span data-ttu-id="37fa1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37fa1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fa1-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37fa1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fa1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37fa1-127">INPUTS</span></span>

### <span data-ttu-id="37fa1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="37fa1-128">System.String</span></span>

## <span data-ttu-id="37fa1-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37fa1-129">OUTPUTS</span></span>

### <span data-ttu-id="37fa1-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="37fa1-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="37fa1-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="37fa1-131">NOTES</span></span>

## <span data-ttu-id="37fa1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37fa1-132">RELATED LINKS</span></span>
