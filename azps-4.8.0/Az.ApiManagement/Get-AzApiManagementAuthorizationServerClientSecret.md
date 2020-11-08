---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113402"
---
# <span data-ttu-id="2aa9c-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="2aa9c-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="2aa9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2aa9c-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa9c-103">Obtém um segredo do cliente do servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="2aa9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2aa9c-104">SYNTAX</span></span>

### <span data-ttu-id="2aa9c-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2aa9c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aa9c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa9c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aa9c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2aa9c-107">DESCRIPTION</span></span>
<span data-ttu-id="2aa9c-108">O cmdlet **Get-AzApiManagementAuthorizationServerClientSecret** Obtém o segredo do cliente do servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="2aa9c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aa9c-109">EXAMPLES</span></span>

### <span data-ttu-id="2aa9c-110">Exemplo 1: obter um segredo de cliente de servidor de autorização especificado por ID</span><span class="sxs-lookup"><span data-stu-id="2aa9c-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="2aa9c-111">Esse comando obtém o servidor de autorização especificado cient segredo.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="2aa9c-112">OS</span><span class="sxs-lookup"><span data-stu-id="2aa9c-112">PARAMETERS</span></span>

### <span data-ttu-id="2aa9c-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2aa9c-113">-Context</span></span>
<span data-ttu-id="2aa9c-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2aa9c-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa9c-116">-DefaultProfile</span></span>
<span data-ttu-id="2aa9c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa9c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa9c-118">-ResourceId</span></span>
<span data-ttu-id="2aa9c-119">Identificador de recursos ARM do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="2aa9c-120">Se especificado, você tentará localizar o servidor de autorização pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="2aa9c-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa9c-122">-ServerID</span><span class="sxs-lookup"><span data-stu-id="2aa9c-122">-ServerId</span></span>
<span data-ttu-id="2aa9c-123">Identificador do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="2aa9c-124">Se especificado, o servidor de autorização será localizado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="2aa9c-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa9c-126">CommonParameters</span></span>
<span data-ttu-id="2aa9c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa9c-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aa9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa9c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2aa9c-129">INPUTS</span></span>

### <span data-ttu-id="2aa9c-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2aa9c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2aa9c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa9c-131">System.String</span></span>

## <span data-ttu-id="2aa9c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2aa9c-132">OUTPUTS</span></span>

### <span data-ttu-id="2aa9c-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="2aa9c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="2aa9c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2aa9c-134">NOTES</span></span>

## <span data-ttu-id="2aa9c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aa9c-135">RELATED LINKS</span></span>
