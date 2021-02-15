---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115295"
---
# <span data-ttu-id="b6cc1-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="b6cc1-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="b6cc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cc1-103">Obtém os conexões do IotHub.</span><span class="sxs-lookup"><span data-stu-id="b6cc1-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="b6cc1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6cc1-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cc1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="b6cc1-106">Obtém os conexões do IotHub.</span><span class="sxs-lookup"><span data-stu-id="b6cc1-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="b6cc1-107">Você pode obter conexões para todas as teclas ou filtre-as por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="b6cc1-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="b6cc1-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6cc1-108">EXAMPLES</span></span>

### <span data-ttu-id="b6cc1-109">Exemplo 1 Obter todos os vínculos de conexão do IotHub</span><span class="sxs-lookup"><span data-stu-id="b6cc1-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b6cc1-110">Obtém os connectionstrings de todas as teclas do iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b6cc1-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="b6cc1-111">Exemplo 2 Obter os vínculos de conexão do IotHub para uma chave específica</span><span class="sxs-lookup"><span data-stu-id="b6cc1-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="b6cc1-112">Obtém os vínculos de conexão da chave chamada "mykey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b6cc1-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="b6cc1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6cc1-113">PARAMETERS</span></span>

### <span data-ttu-id="b6cc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cc1-114">-DefaultProfile</span></span>
<span data-ttu-id="b6cc1-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b6cc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6cc1-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b6cc1-116">-KeyName</span></span>
<span data-ttu-id="b6cc1-117">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="b6cc1-117">Name of the Key</span></span>

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

### <span data-ttu-id="b6cc1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6cc1-118">-Name</span></span>
<span data-ttu-id="b6cc1-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="b6cc1-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="b6cc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6cc1-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b6cc1-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b6cc1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cc1-122">CommonParameters</span></span>
<span data-ttu-id="b6cc1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cc1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cc1-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cc1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cc1-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6cc1-125">INPUTS</span></span>

### <span data-ttu-id="b6cc1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b6cc1-126">System.String</span></span>

## <span data-ttu-id="b6cc1-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6cc1-127">OUTPUTS</span></span>

### <span data-ttu-id="b6cc1-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b6cc1-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b6cc1-129">Notas</span><span class="sxs-lookup"><span data-stu-id="b6cc1-129">NOTES</span></span>

## <span data-ttu-id="b6cc1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6cc1-130">RELATED LINKS</span></span>
