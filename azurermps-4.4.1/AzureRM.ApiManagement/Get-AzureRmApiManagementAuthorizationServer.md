---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431845"
---
# <span data-ttu-id="958ce-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="958ce-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="958ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="958ce-102">SYNOPSIS</span></span>
<span data-ttu-id="958ce-103">Obtém um servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="958ce-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="958ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="958ce-104">SYNTAX</span></span>

### <span data-ttu-id="958ce-105">Obter todo o servidor de autorização (padrão)</span><span class="sxs-lookup"><span data-stu-id="958ce-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958ce-106">Obter por ID</span><span class="sxs-lookup"><span data-stu-id="958ce-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="958ce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="958ce-107">DESCRIPTION</span></span>
<span data-ttu-id="958ce-108">O cmdlet **Get-AzureRmApiManagementAuthorizationServer** Obtém todos os servidores de autorização de gerenciamento de API do Azure ou servidores de autorização especificados.</span><span class="sxs-lookup"><span data-stu-id="958ce-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="958ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="958ce-109">EXAMPLES</span></span>

### <span data-ttu-id="958ce-110">Exemplo 1: obter todos os servidores de autorização</span><span class="sxs-lookup"><span data-stu-id="958ce-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="958ce-111">Esse comando obtém todos os servidores de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="958ce-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="958ce-112">Exemplo 2: obter um servidor de autorização especificado</span><span class="sxs-lookup"><span data-stu-id="958ce-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="958ce-113">Esse comando obtém o servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="958ce-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="958ce-114">OS</span><span class="sxs-lookup"><span data-stu-id="958ce-114">PARAMETERS</span></span>

### <span data-ttu-id="958ce-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="958ce-115">-Context</span></span>
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

### <span data-ttu-id="958ce-116">-ServerID</span><span class="sxs-lookup"><span data-stu-id="958ce-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958ce-117">-DefaultProfile</span></span>
<span data-ttu-id="958ce-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="958ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="958ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958ce-119">CommonParameters</span></span>
<span data-ttu-id="958ce-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958ce-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958ce-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="958ce-122">INPUTS</span></span>

## <span data-ttu-id="958ce-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="958ce-123">OUTPUTS</span></span>

### <span data-ttu-id="958ce-124">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="958ce-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="958ce-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="958ce-125">NOTES</span></span>

## <span data-ttu-id="958ce-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="958ce-126">RELATED LINKS</span></span>

[<span data-ttu-id="958ce-127">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="958ce-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="958ce-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="958ce-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="958ce-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="958ce-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


