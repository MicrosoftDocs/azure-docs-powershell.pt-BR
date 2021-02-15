---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118092"
---
# <span data-ttu-id="0e517-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="0e517-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="0e517-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e517-102">SYNOPSIS</span></span>
<span data-ttu-id="0e517-103">Obtém um segredo do cliente de servidor de autorização de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0e517-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="0e517-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e517-104">SYNTAX</span></span>

### <span data-ttu-id="0e517-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e517-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e517-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e517-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e517-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e517-107">DESCRIPTION</span></span>
<span data-ttu-id="0e517-108">O cmdlet **Get-AzApiManagementAuthorizationServerClientSec ltd** obtém o segredo do cliente do servidor de autorização do Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e517-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="0e517-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e517-109">EXAMPLES</span></span>

### <span data-ttu-id="0e517-110">Exemplo 1: Obter um segredo de cliente de servidor de autorização especificado por id</span><span class="sxs-lookup"><span data-stu-id="0e517-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="0e517-111">Esse comando obtém o segredo de servidor de autorização especificado.</span><span class="sxs-lookup"><span data-stu-id="0e517-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="0e517-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e517-112">PARAMETERS</span></span>

### <span data-ttu-id="0e517-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0e517-113">-Context</span></span>
<span data-ttu-id="0e517-114">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0e517-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0e517-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0e517-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0e517-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e517-116">-DefaultProfile</span></span>
<span data-ttu-id="0e517-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e517-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e517-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e517-118">-ResourceId</span></span>
<span data-ttu-id="0e517-119">Arm Resource Identifier do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="0e517-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="0e517-120">Se especificado, tentará encontrar o servidor de autorização pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="0e517-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="0e517-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0e517-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0e517-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="0e517-122">-ServerId</span></span>
<span data-ttu-id="0e517-123">Identificador do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="0e517-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="0e517-124">Se especificado, o identificador encontrará o servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="0e517-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="0e517-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e517-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="0e517-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e517-126">CommonParameters</span></span>
<span data-ttu-id="0e517-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e517-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e517-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e517-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e517-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e517-129">INPUTS</span></span>

### <span data-ttu-id="0e517-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0e517-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0e517-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0e517-131">System.String</span></span>

## <span data-ttu-id="0e517-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e517-132">OUTPUTS</span></span>

### <span data-ttu-id="0e517-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSec limited</span><span class="sxs-lookup"><span data-stu-id="0e517-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="0e517-134">Notas</span><span class="sxs-lookup"><span data-stu-id="0e517-134">NOTES</span></span>

## <span data-ttu-id="0e517-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e517-135">RELATED LINKS</span></span>
