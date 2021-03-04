---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 098fb692e1710b9463650f0e398d999f0a2b1062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889357"
---
# <span data-ttu-id="a1f4c-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a1f4c-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="a1f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f4c-103">Obtém um servidor de autorização de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="a1f4c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1f4c-104">SYNTAX</span></span>

### <span data-ttu-id="a1f4c-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1f4c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f4c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1f4c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f4c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="a1f4c-108">O cmdlet **Get-AzApiManagementAuthorizationServer** obtém todos os servidores de autorização de Gerenciamento de API do Azure ou servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="a1f4c-109">ClientSecret não será incluído nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="a1f4c-110">Para obter o segredo do cliente, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="a1f4c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-111">EXAMPLES</span></span>

### <span data-ttu-id="a1f4c-112">Exemplo 1: Obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="a1f4c-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="a1f4c-113">Este comando obtém todos os servidores de autorização de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="a1f4c-114">Exemplo 2: Obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="a1f4c-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="a1f4c-115">Este comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="a1f4c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-116">PARAMETERS</span></span>

### <span data-ttu-id="a1f4c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a1f4c-117">-Context</span></span>

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

### <span data-ttu-id="a1f4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f4c-118">-DefaultProfile</span></span>
<span data-ttu-id="a1f4c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1f4c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1f4c-120">-ResourceId</span></span>
<span data-ttu-id="a1f4c-121">Arm Resource Identifier do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="a1f4c-122">Se especificado, tentará encontrar o servidor de autorização pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="a1f4c-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a1f4c-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="a1f4c-124">-ServerId</span></span>
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

### <span data-ttu-id="a1f4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f4c-125">CommonParameters</span></span>
<span data-ttu-id="a1f4c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f4c-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1f4c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f4c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-128">INPUTS</span></span>

### <span data-ttu-id="a1f4c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1f4c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1f4c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a1f4c-130">System.String</span></span>

## <span data-ttu-id="a1f4c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-131">OUTPUTS</span></span>

### <span data-ttu-id="a1f4c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a1f4c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="a1f4c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1f4c-133">NOTES</span></span>

## <span data-ttu-id="a1f4c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1f4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1f4c-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a1f4c-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="a1f4c-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a1f4c-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="a1f4c-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a1f4c-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


