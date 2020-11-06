---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598122"
---
# <span data-ttu-id="e1890-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e1890-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="e1890-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1890-102">SYNOPSIS</span></span>
<span data-ttu-id="e1890-103">Obtém um servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e1890-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="e1890-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1890-104">SYNTAX</span></span>

### <span data-ttu-id="e1890-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1890-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1890-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1890-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1890-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1890-107">DESCRIPTION</span></span>
<span data-ttu-id="e1890-108">O cmdlet **Get-AzApiManagementAuthorizationServer** Obtém todos os servidores de autorização de gerenciamento de API do Azure ou servidores de autorização especificados.</span><span class="sxs-lookup"><span data-stu-id="e1890-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="e1890-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1890-109">EXAMPLES</span></span>

### <span data-ttu-id="e1890-110">Exemplo 1: obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="e1890-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="e1890-111">Esse comando obtém todos os servidores de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e1890-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="e1890-112">Exemplo 2: obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="e1890-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="e1890-113">Esse comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="e1890-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="e1890-114">OS</span><span class="sxs-lookup"><span data-stu-id="e1890-114">PARAMETERS</span></span>

### <span data-ttu-id="e1890-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e1890-115">-Context</span></span>

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

### <span data-ttu-id="e1890-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1890-116">-DefaultProfile</span></span>
<span data-ttu-id="e1890-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1890-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1890-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1890-118">-ResourceId</span></span>
<span data-ttu-id="e1890-119">Identificador de recursos ARM do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="e1890-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="e1890-120">Se especificado, você tentará localizar o servidor de autorização pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="e1890-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="e1890-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e1890-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e1890-122">-ServerID</span><span class="sxs-lookup"><span data-stu-id="e1890-122">-ServerId</span></span>
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

### <span data-ttu-id="e1890-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1890-123">CommonParameters</span></span>
<span data-ttu-id="e1890-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1890-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1890-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1890-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1890-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1890-126">INPUTS</span></span>

### <span data-ttu-id="e1890-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1890-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1890-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e1890-128">System.String</span></span>

## <span data-ttu-id="e1890-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1890-129">OUTPUTS</span></span>

### <span data-ttu-id="e1890-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e1890-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="e1890-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1890-131">NOTES</span></span>

## <span data-ttu-id="e1890-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1890-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1890-133">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e1890-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e1890-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e1890-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e1890-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e1890-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


