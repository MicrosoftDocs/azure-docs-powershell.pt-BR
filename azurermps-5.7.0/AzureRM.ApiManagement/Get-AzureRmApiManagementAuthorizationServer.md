---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603288"
---
# <span data-ttu-id="2ce98-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2ce98-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="2ce98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ce98-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce98-103">Obtém um servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2ce98-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ce98-104">SYNTAX</span></span>

### <span data-ttu-id="2ce98-105">GetAllAuthorizationServers (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ce98-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ce98-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="2ce98-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ce98-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ce98-107">DESCRIPTION</span></span>
<span data-ttu-id="2ce98-108">O cmdlet **Get-AzureRmApiManagementAuthorizationServer** Obtém todos os servidores de autorização de gerenciamento de API do Azure ou servidores de autorização especificados.</span><span class="sxs-lookup"><span data-stu-id="2ce98-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="2ce98-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ce98-109">EXAMPLES</span></span>

### <span data-ttu-id="2ce98-110">Exemplo 1: obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="2ce98-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="2ce98-111">Esse comando obtém todos os servidores de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2ce98-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="2ce98-112">Exemplo 2: obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="2ce98-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="2ce98-113">Esse comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="2ce98-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="2ce98-114">OS</span><span class="sxs-lookup"><span data-stu-id="2ce98-114">PARAMETERS</span></span>

### <span data-ttu-id="2ce98-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2ce98-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce98-116">-DefaultProfile</span></span>
<span data-ttu-id="2ce98-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce98-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce98-118">-ServerID</span><span class="sxs-lookup"><span data-stu-id="2ce98-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce98-119">CommonParameters</span></span>
<span data-ttu-id="2ce98-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce98-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce98-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce98-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ce98-122">INPUTS</span></span>

### <span data-ttu-id="2ce98-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ce98-123">None</span></span>
<span data-ttu-id="2ce98-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2ce98-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ce98-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ce98-125">OUTPUTS</span></span>

### <span data-ttu-id="2ce98-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="2ce98-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="2ce98-127">Os detalhes do servidor de autorização em um determinado serviço de gerenciamento de APIs.</span><span class="sxs-lookup"><span data-stu-id="2ce98-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="2ce98-128">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="2ce98-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="2ce98-129">A lista de servidores de autorização em um determinado serviço de gerenciamento de APIs.</span><span class="sxs-lookup"><span data-stu-id="2ce98-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="2ce98-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ce98-130">NOTES</span></span>

## <span data-ttu-id="2ce98-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ce98-131">RELATED LINKS</span></span>

[<span data-ttu-id="2ce98-132">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2ce98-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="2ce98-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2ce98-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="2ce98-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2ce98-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


