---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595690"
---
# <span data-ttu-id="f33ac-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f33ac-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="f33ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f33ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f33ac-103">Obtém um servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f33ac-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="f33ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f33ac-104">SYNTAX</span></span>

### <span data-ttu-id="f33ac-105">GetAllAuthorizationServers (padrão)</span><span class="sxs-lookup"><span data-stu-id="f33ac-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f33ac-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="f33ac-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f33ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f33ac-107">DESCRIPTION</span></span>
<span data-ttu-id="f33ac-108">O cmdlet **Get-AzApiManagementAuthorizationServer** Obtém todos os servidores de autorização de gerenciamento de API do Azure ou servidores de autorização especificados.</span><span class="sxs-lookup"><span data-stu-id="f33ac-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="f33ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f33ac-109">EXAMPLES</span></span>

### <span data-ttu-id="f33ac-110">Exemplo 1: obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="f33ac-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="f33ac-111">Esse comando obtém todos os servidores de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f33ac-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="f33ac-112">Exemplo 2: obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="f33ac-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="f33ac-113">Esse comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="f33ac-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="f33ac-114">OS</span><span class="sxs-lookup"><span data-stu-id="f33ac-114">PARAMETERS</span></span>

### <span data-ttu-id="f33ac-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f33ac-115">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f33ac-116">-DefaultProfile</span></span>
<span data-ttu-id="f33ac-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f33ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f33ac-118">-ServerID</span><span class="sxs-lookup"><span data-stu-id="f33ac-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33ac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33ac-119">CommonParameters</span></span>
<span data-ttu-id="f33ac-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f33ac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33ac-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33ac-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33ac-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f33ac-122">INPUTS</span></span>

### <span data-ttu-id="f33ac-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f33ac-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f33ac-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f33ac-124">System.String</span></span>

## <span data-ttu-id="f33ac-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f33ac-125">OUTPUTS</span></span>

### <span data-ttu-id="f33ac-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="f33ac-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="f33ac-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f33ac-127">NOTES</span></span>

## <span data-ttu-id="f33ac-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f33ac-128">RELATED LINKS</span></span>

[<span data-ttu-id="f33ac-129">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f33ac-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f33ac-130">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f33ac-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f33ac-131">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f33ac-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


