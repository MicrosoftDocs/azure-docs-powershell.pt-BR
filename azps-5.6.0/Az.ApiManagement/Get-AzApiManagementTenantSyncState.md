---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: d253c1da05bd62e40dcdddaa90033512b3932d27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892260"
---
# <span data-ttu-id="0ad57-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="0ad57-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="0ad57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad57-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad57-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório git.</span><span class="sxs-lookup"><span data-stu-id="0ad57-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0ad57-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0ad57-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad57-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0ad57-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad57-106">O cmdlet **Get-AzApiManagementTenantSyncState** obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do Git.</span><span class="sxs-lookup"><span data-stu-id="0ad57-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0ad57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ad57-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad57-108">Exemplo 1: Obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="0ad57-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="0ad57-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório git.</span><span class="sxs-lookup"><span data-stu-id="0ad57-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0ad57-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0ad57-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad57-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0ad57-111">-Context</span></span>
<span data-ttu-id="0ad57-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0ad57-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0ad57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad57-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad57-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0ad57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad57-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad57-115">CommonParameters</span></span>
<span data-ttu-id="0ad57-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad57-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad57-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ad57-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad57-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ad57-118">INPUTS</span></span>

### <span data-ttu-id="0ad57-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0ad57-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="0ad57-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0ad57-120">OUTPUTS</span></span>

### <span data-ttu-id="0ad57-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="0ad57-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="0ad57-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="0ad57-122">NOTES</span></span>

## <span data-ttu-id="0ad57-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ad57-123">RELATED LINKS</span></span>
