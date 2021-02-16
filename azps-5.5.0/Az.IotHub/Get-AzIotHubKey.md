---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113140"
---
# <span data-ttu-id="b4c8f-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b4c8f-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="b4c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c8f-103">Obtém uma tecla IotHub.</span><span class="sxs-lookup"><span data-stu-id="b4c8f-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="b4c8f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4c8f-104">SYNTAX</span></span>

### <span data-ttu-id="b4c8f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4c8f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c8f-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4c8f-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4c8f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4c8f-107">DESCRIPTION</span></span>
<span data-ttu-id="b4c8f-108">Obtém uma tecla IotHub.</span><span class="sxs-lookup"><span data-stu-id="b4c8f-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="b4c8f-109">Você pode listar todas as Teclas ou filtrar a lista por um Nome de Chave específico.</span><span class="sxs-lookup"><span data-stu-id="b4c8f-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="b4c8f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4c8f-110">EXAMPLES</span></span>

### <span data-ttu-id="b4c8f-111">Exemplo 1 Obter todas as teclas</span><span class="sxs-lookup"><span data-stu-id="b4c8f-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b4c8f-112">Obtém todas as Teclas do IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b4c8f-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="b4c8f-113">Exemplo 2 Obter informações para uma chave específica</span><span class="sxs-lookup"><span data-stu-id="b4c8f-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="b4c8f-114">Obtém as informações de uma chave chamada "iothu bowlner" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b4c8f-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b4c8f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4c8f-115">PARAMETERS</span></span>

### <span data-ttu-id="b4c8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c8f-116">-DefaultProfile</span></span>
<span data-ttu-id="b4c8f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b4c8f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4c8f-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="b4c8f-118">-HubId</span></span>
<span data-ttu-id="b4c8f-119">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="b4c8f-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b4c8f-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b4c8f-120">-KeyName</span></span>
<span data-ttu-id="b4c8f-121">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="b4c8f-121">Name of the Key</span></span>

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

### <span data-ttu-id="b4c8f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4c8f-122">-Name</span></span>
<span data-ttu-id="b4c8f-123">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="b4c8f-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b4c8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4c8f-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b4c8f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b4c8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c8f-126">CommonParameters</span></span>
<span data-ttu-id="b4c8f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4c8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c8f-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4c8f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c8f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4c8f-129">INPUTS</span></span>

### <span data-ttu-id="b4c8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b4c8f-130">System.String</span></span>

## <span data-ttu-id="b4c8f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4c8f-131">OUTPUTS</span></span>

### <span data-ttu-id="b4c8f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4c8f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b4c8f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b4c8f-133">NOTES</span></span>

## <span data-ttu-id="b4c8f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4c8f-134">RELATED LINKS</span></span>
