---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115371"
---
# <span data-ttu-id="80dc4-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="80dc4-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="80dc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="80dc4-103">Crie uma nova instância detalhes do aplicativo DataMigration Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="80dc4-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="80dc4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80dc4-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80dc4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="80dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="80dc4-106">Crie uma nova instância detalhes do aplicativo DataMigration Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="80dc4-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="80dc4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="80dc4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80dc4-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="80dc4-109">ApplicationId : "Sua ID do AppId/Service Principal aqui" AppKey: System.Security.SecureString TenantId: "ID do locatário"</span><span class="sxs-lookup"><span data-stu-id="80dc4-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="80dc4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="80dc4-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="80dc4-111">-AppKey</span></span>
<span data-ttu-id="80dc4-112">Chave do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="80dc4-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80dc4-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="80dc4-113">-ApplicationId</span></span>
<span data-ttu-id="80dc4-114">ID do Aplicativo do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="80dc4-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80dc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dc4-115">-DefaultProfile</span></span>
<span data-ttu-id="80dc4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80dc4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dc4-117">CommonParameters</span></span>
<span data-ttu-id="80dc4-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80dc4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80dc4-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dc4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dc4-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="80dc4-120">INPUTS</span></span>

### <span data-ttu-id="80dc4-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="80dc4-121">None</span></span>

## <span data-ttu-id="80dc4-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="80dc4-122">OUTPUTS</span></span>

### <span data-ttu-id="80dc4-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="80dc4-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="80dc4-124">Notas</span><span class="sxs-lookup"><span data-stu-id="80dc4-124">NOTES</span></span>

## <span data-ttu-id="80dc4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80dc4-125">RELATED LINKS</span></span>
