---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114844"
---
# <span data-ttu-id="8e2cc-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="8e2cc-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="8e2cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2cc-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório git.</span><span class="sxs-lookup"><span data-stu-id="8e2cc-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="8e2cc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e2cc-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2cc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e2cc-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2cc-106">O cmdlet **Get-AzApiManagementTenantSyncState** obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório git.</span><span class="sxs-lookup"><span data-stu-id="8e2cc-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="8e2cc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e2cc-107">EXAMPLES</span></span>

### <span data-ttu-id="8e2cc-108">Exemplo 1: Obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="8e2cc-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="8e2cc-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório Git.</span><span class="sxs-lookup"><span data-stu-id="8e2cc-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="8e2cc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e2cc-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2cc-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8e2cc-111">-Context</span></span>
<span data-ttu-id="8e2cc-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8e2cc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8e2cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2cc-113">-DefaultProfile</span></span>
<span data-ttu-id="8e2cc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8e2cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2cc-115">CommonParameters</span></span>
<span data-ttu-id="8e2cc-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2cc-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e2cc-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2cc-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e2cc-118">INPUTS</span></span>

### <span data-ttu-id="8e2cc-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e2cc-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="8e2cc-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e2cc-120">OUTPUTS</span></span>

### <span data-ttu-id="8e2cc-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="8e2cc-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="8e2cc-122">Notas</span><span class="sxs-lookup"><span data-stu-id="8e2cc-122">NOTES</span></span>

## <span data-ttu-id="8e2cc-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e2cc-123">RELATED LINKS</span></span>
