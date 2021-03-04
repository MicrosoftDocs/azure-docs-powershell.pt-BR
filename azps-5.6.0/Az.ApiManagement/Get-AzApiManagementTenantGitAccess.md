---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 29e15515dfb5c8db53255cd283573fec11239940
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892263"
---
# <span data-ttu-id="08450-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="08450-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="08450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08450-102">SYNOPSIS</span></span>
<span data-ttu-id="08450-103">Obtém a configuração de acesso do Git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="08450-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="08450-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="08450-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08450-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="08450-105">DESCRIPTION</span></span>
<span data-ttu-id="08450-106">O cmdlet **Get-AzApiManagementTenantGitAccess** obtém a configuração de acesso do Git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="08450-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="08450-107">As chaves não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="08450-107">Keys will not be included into result details.</span></span> <span data-ttu-id="08450-108">Para obter o segredo do cliente, use **Get-AzApiManagementTenantGitAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="08450-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="08450-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08450-109">EXAMPLES</span></span>

### <span data-ttu-id="08450-110">Exemplo 1: Obter configuração de acesso de locatário</span><span class="sxs-lookup"><span data-stu-id="08450-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="08450-111">Este comando obtém a configuração de acesso do Git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="08450-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="08450-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="08450-112">PARAMETERS</span></span>

### <span data-ttu-id="08450-113">-Context</span><span class="sxs-lookup"><span data-stu-id="08450-113">-Context</span></span>
<span data-ttu-id="08450-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="08450-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08450-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08450-115">-DefaultProfile</span></span>
<span data-ttu-id="08450-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="08450-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08450-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08450-117">CommonParameters</span></span>
<span data-ttu-id="08450-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08450-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08450-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08450-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08450-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08450-120">INPUTS</span></span>

### <span data-ttu-id="08450-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08450-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="08450-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="08450-122">OUTPUTS</span></span>

### <span data-ttu-id="08450-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="08450-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="08450-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="08450-124">NOTES</span></span>

## <span data-ttu-id="08450-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08450-125">RELATED LINKS</span></span>
