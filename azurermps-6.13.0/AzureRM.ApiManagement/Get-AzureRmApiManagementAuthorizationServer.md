---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2e18be1721f68a0e1223bf45b9ca2e637c05a378
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431475"
---
# <span data-ttu-id="9e6d8-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9e6d8-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="9e6d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6d8-103">Obtém um servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e6d8-104">SYNTAX</span></span>

### <span data-ttu-id="9e6d8-105">GetAllAuthorizationServers (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e6d8-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e6d8-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="9e6d8-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6d8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e6d8-107">DESCRIPTION</span></span>
<span data-ttu-id="9e6d8-108">O cmdlet **Get-AzureRmApiManagementAuthorizationServer** Obtém todos os servidores de autorização de gerenciamento de API do Azure ou servidores de autorização especificados.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="9e6d8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e6d8-109">EXAMPLES</span></span>

### <span data-ttu-id="9e6d8-110">Exemplo 1: obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="9e6d8-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="9e6d8-111">Esse comando obtém todos os servidores de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="9e6d8-112">Exemplo 2: obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="9e6d8-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="9e6d8-113">Esse comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="9e6d8-114">OS</span><span class="sxs-lookup"><span data-stu-id="9e6d8-114">PARAMETERS</span></span>

### <span data-ttu-id="9e6d8-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9e6d8-115">-Context</span></span>

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

### <span data-ttu-id="9e6d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6d8-116">-DefaultProfile</span></span>
<span data-ttu-id="9e6d8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e6d8-118">-ServerID</span><span class="sxs-lookup"><span data-stu-id="9e6d8-118">-ServerId</span></span>
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

### <span data-ttu-id="9e6d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6d8-119">CommonParameters</span></span>
<span data-ttu-id="9e6d8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6d8-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6d8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6d8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e6d8-122">INPUTS</span></span>

### <span data-ttu-id="9e6d8-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e6d8-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e6d8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6d8-124">System.String</span></span>

## <span data-ttu-id="9e6d8-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e6d8-125">OUTPUTS</span></span>

### <span data-ttu-id="9e6d8-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="9e6d8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="9e6d8-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e6d8-127">NOTES</span></span>

## <span data-ttu-id="9e6d8-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e6d8-128">RELATED LINKS</span></span>

[<span data-ttu-id="9e6d8-129">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9e6d8-129">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="9e6d8-130">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9e6d8-130">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="9e6d8-131">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9e6d8-131">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


