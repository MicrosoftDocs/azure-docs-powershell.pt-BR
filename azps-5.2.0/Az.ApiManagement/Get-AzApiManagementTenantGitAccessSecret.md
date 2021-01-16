---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263091"
---
# <span data-ttu-id="80742-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="80742-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="80742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80742-102">SYNOPSIS</span></span>
<span data-ttu-id="80742-103">Obtém as chaves de configuração de acesso git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="80742-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="80742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80742-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80742-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80742-105">DESCRIPTION</span></span>
<span data-ttu-id="80742-106">Obtém as chaves de configuração de acesso git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="80742-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="80742-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80742-107">EXAMPLES</span></span>

### <span data-ttu-id="80742-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="80742-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="80742-109">Este comando obtém as chaves de configuração de acesso git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="80742-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="80742-110">OS</span><span class="sxs-lookup"><span data-stu-id="80742-110">PARAMETERS</span></span>

### <span data-ttu-id="80742-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="80742-111">-Context</span></span>
<span data-ttu-id="80742-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="80742-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80742-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="80742-113">This parameter is required.</span></span>

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

### <span data-ttu-id="80742-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80742-114">-DefaultProfile</span></span>
<span data-ttu-id="80742-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80742-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80742-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80742-116">CommonParameters</span></span>
<span data-ttu-id="80742-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80742-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80742-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80742-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80742-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80742-119">INPUTS</span></span>

### <span data-ttu-id="80742-120">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80742-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="80742-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80742-121">OUTPUTS</span></span>

### <span data-ttu-id="80742-122">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="80742-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="80742-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80742-123">NOTES</span></span>

## <span data-ttu-id="80742-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80742-124">RELATED LINKS</span></span>
