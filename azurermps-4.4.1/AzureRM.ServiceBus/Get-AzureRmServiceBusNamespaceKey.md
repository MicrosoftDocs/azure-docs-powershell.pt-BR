---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430628"
---
# <span data-ttu-id="7d855-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="7d855-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="7d855-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d855-102">SYNOPSIS</span></span>
<span data-ttu-id="7d855-103">Obtém as cadeias de conexão primária e secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="7d855-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d855-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d855-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d855-105">DESCRIPTION</span></span>
<span data-ttu-id="7d855-106">O cmdlet **Get-AzureRmServiceBusNamespaceKey** retorna as cadeias de conexão primária e secundária para o namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="7d855-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="7d855-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d855-107">EXAMPLES</span></span>

### <span data-ttu-id="7d855-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d855-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="7d855-109">Cadeia de conexão primária e secundária para o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="7d855-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="7d855-110">OS</span><span class="sxs-lookup"><span data-stu-id="7d855-110">PARAMETERS</span></span>

### <span data-ttu-id="7d855-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="7d855-111">-ResourceGroup</span></span>
<span data-ttu-id="7d855-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d855-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d855-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d855-113">-DefaultProfile</span></span>
<span data-ttu-id="7d855-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d855-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d855-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d855-115">-Name</span></span>
<span data-ttu-id="7d855-116">Nome do namespace do ServiceBus AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7d855-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d855-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d855-117">-Namespace</span></span>
<span data-ttu-id="7d855-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="7d855-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d855-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d855-119">CommonParameters</span></span>
<span data-ttu-id="7d855-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d855-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d855-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d855-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d855-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d855-122">INPUTS</span></span>

### <span data-ttu-id="7d855-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="7d855-123">-ResourceGroup</span></span>
 <span data-ttu-id="7d855-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7d855-124">System.String</span></span>
 

### <span data-ttu-id="7d855-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7d855-125">-NamespaceName</span></span>
 <span data-ttu-id="7d855-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7d855-126">System.String</span></span>
 

### <span data-ttu-id="7d855-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7d855-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7d855-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7d855-128">System.String</span></span>

## <span data-ttu-id="7d855-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d855-129">OUTPUTS</span></span>

### <span data-ttu-id="7d855-130">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="7d855-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="7d855-131">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey valor} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey valor} PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey valor} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7d855-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="7d855-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d855-132">NOTES</span></span>

## <span data-ttu-id="7d855-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d855-133">RELATED LINKS</span></span>

