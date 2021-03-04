---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892261"
---
# <span data-ttu-id="b2bc6-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b2bc6-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="b2bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bc6-103">Obtém as chaves de configuração de acesso do Git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b2bc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2bc6-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bc6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2bc6-105">DESCRIPTION</span></span>
<span data-ttu-id="b2bc6-106">Obtém as chaves de configuração de acesso do Git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b2bc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-107">EXAMPLES</span></span>

### <span data-ttu-id="b2bc6-108">Exemplo 1: Obter configuração de acesso de locatário</span><span class="sxs-lookup"><span data-stu-id="b2bc6-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="b2bc6-109">Este comando obtém as chaves de configuração de acesso do Git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b2bc6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-110">PARAMETERS</span></span>

### <span data-ttu-id="b2bc6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b2bc6-111">-Context</span></span>
<span data-ttu-id="b2bc6-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b2bc6-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b2bc6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bc6-114">-DefaultProfile</span></span>
<span data-ttu-id="b2bc6-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2bc6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bc6-116">CommonParameters</span></span>
<span data-ttu-id="b2bc6-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bc6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bc6-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2bc6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bc6-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-119">INPUTS</span></span>

### <span data-ttu-id="b2bc6-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2bc6-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b2bc6-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-121">OUTPUTS</span></span>

### <span data-ttu-id="b2bc6-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b2bc6-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b2bc6-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2bc6-123">NOTES</span></span>

## <span data-ttu-id="b2bc6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2bc6-124">RELATED LINKS</span></span>
