---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 4a63f13e567a5f53726058c831107ce43768c0f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889947"
---
# <span data-ttu-id="e8cf9-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e8cf9-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="e8cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cf9-103">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="e8cf9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8cf9-104">SYNTAX</span></span>

### <span data-ttu-id="e8cf9-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8cf9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cf9-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8cf9-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8cf9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="e8cf9-108">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="e8cf9-109">Você pode listar todas as Chaves ou filtrar a lista por um Nome de Chave específico.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="e8cf9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-110">EXAMPLES</span></span>

### <span data-ttu-id="e8cf9-111">Exemplo 1 Obter todas as chaves</span><span class="sxs-lookup"><span data-stu-id="e8cf9-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e8cf9-112">Obtém todas as chaves do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e8cf9-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e8cf9-113">Exemplo 2 Obter informações para uma chave específica</span><span class="sxs-lookup"><span data-stu-id="e8cf9-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="e8cf9-114">Obtém as informações de uma chave chamada "iothubowner" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e8cf9-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e8cf9-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-115">PARAMETERS</span></span>

### <span data-ttu-id="e8cf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cf9-116">-DefaultProfile</span></span>
<span data-ttu-id="e8cf9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e8cf9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8cf9-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="e8cf9-118">-HubId</span></span>
<span data-ttu-id="e8cf9-119">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="e8cf9-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e8cf9-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e8cf9-120">-KeyName</span></span>
<span data-ttu-id="e8cf9-121">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="e8cf9-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cf9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8cf9-122">-Name</span></span>
<span data-ttu-id="e8cf9-123">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8cf9-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e8cf9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e8cf9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cf9-126">CommonParameters</span></span>
<span data-ttu-id="e8cf9-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cf9-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8cf9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cf9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-129">INPUTS</span></span>

### <span data-ttu-id="e8cf9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e8cf9-130">System.String</span></span>

## <span data-ttu-id="e8cf9-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-131">OUTPUTS</span></span>

### <span data-ttu-id="e8cf9-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e8cf9-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e8cf9-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8cf9-133">NOTES</span></span>

## <span data-ttu-id="e8cf9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8cf9-134">RELATED LINKS</span></span>
