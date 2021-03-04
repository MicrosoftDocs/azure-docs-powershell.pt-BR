---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889967"
---
# <span data-ttu-id="b9e97-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="b9e97-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="b9e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e97-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e97-103">Obtém as conexões IotHub.</span><span class="sxs-lookup"><span data-stu-id="b9e97-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="b9e97-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9e97-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e97-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9e97-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e97-106">Obtém as conexões IotHub.</span><span class="sxs-lookup"><span data-stu-id="b9e97-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="b9e97-107">Você pode obter connectionstrings para todas as chaves ou filtre-as por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="b9e97-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="b9e97-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e97-108">EXAMPLES</span></span>

### <span data-ttu-id="b9e97-109">Exemplo 1 Get All IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="b9e97-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b9e97-110">Obtém os connectionstrings de todas as chaves do iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b9e97-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="b9e97-111">Exemplo 2 Obter os connectionstrings do IotHub para uma chave específica</span><span class="sxs-lookup"><span data-stu-id="b9e97-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="b9e97-112">Obtém os connectionstrings da chave chamada "mykey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b9e97-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="b9e97-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9e97-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e97-114">-DefaultProfile</span></span>
<span data-ttu-id="b9e97-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b9e97-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e97-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b9e97-116">-KeyName</span></span>
<span data-ttu-id="b9e97-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="b9e97-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e97-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b9e97-118">-Name</span></span>
<span data-ttu-id="b9e97-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="b9e97-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="b9e97-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e97-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9e97-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b9e97-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b9e97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e97-122">CommonParameters</span></span>
<span data-ttu-id="b9e97-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e97-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e97-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e97-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9e97-125">INPUTS</span></span>

### <span data-ttu-id="b9e97-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b9e97-126">System.String</span></span>

## <span data-ttu-id="b9e97-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9e97-127">OUTPUTS</span></span>

### <span data-ttu-id="b9e97-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b9e97-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b9e97-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9e97-129">NOTES</span></span>

## <span data-ttu-id="b9e97-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e97-130">RELATED LINKS</span></span>
