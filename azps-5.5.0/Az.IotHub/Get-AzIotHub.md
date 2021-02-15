---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114827"
---
# <span data-ttu-id="0becb-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="0becb-101">Get-AzIotHub</span></span>

## <span data-ttu-id="0becb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0becb-102">SYNOPSIS</span></span>
<span data-ttu-id="0becb-103">Obtém informações sobre os IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0becb-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="0becb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0becb-104">SYNTAX</span></span>

### <span data-ttu-id="0becb-105">ListIotHubsByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0becb-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0becb-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="0becb-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0becb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0becb-107">DESCRIPTION</span></span>
<span data-ttu-id="0becb-108">Obtém informações sobre os IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0becb-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="0becb-109">Você pode exibir todas as instâncias do IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome específico do IotHub.</span><span class="sxs-lookup"><span data-stu-id="0becb-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="0becb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0becb-110">EXAMPLES</span></span>

### <span data-ttu-id="0becb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0becb-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="0becb-112">Obtém todos os IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="0becb-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="0becb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0becb-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="0becb-114">Obtém todos os IotHubs da assinatura que pertencem ao grupo de recursos chamado "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="0becb-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="0becb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0becb-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0becb-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="0becb-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="0becb-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0becb-117">PARAMETERS</span></span>

### <span data-ttu-id="0becb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0becb-118">-DefaultProfile</span></span>
<span data-ttu-id="0becb-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0becb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0becb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0becb-120">-Name</span></span>
<span data-ttu-id="0becb-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="0becb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="0becb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0becb-122">-ResourceGroupName</span></span>
<span data-ttu-id="0becb-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0becb-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="0becb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0becb-124">CommonParameters</span></span>
<span data-ttu-id="0becb-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0becb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0becb-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0becb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0becb-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="0becb-127">INPUTS</span></span>

### <span data-ttu-id="0becb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0becb-128">System.String</span></span>

## <span data-ttu-id="0becb-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="0becb-129">OUTPUTS</span></span>

### <span data-ttu-id="0becb-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0becb-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="0becb-131">Notas</span><span class="sxs-lookup"><span data-stu-id="0becb-131">NOTES</span></span>

## <span data-ttu-id="0becb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0becb-132">RELATED LINKS</span></span>
