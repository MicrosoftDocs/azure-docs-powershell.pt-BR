---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 7d62a005455394dd1b00309adcf47bc639551a4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429665"
---
# <span data-ttu-id="d59f5-101">Get-AzureRmSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d59f5-101">Get-AzureRmSqlCapability</span></span>

## <span data-ttu-id="d59f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d59f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d59f5-103">Obtém recursos de banco de dados SQL para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d59f5-103">Gets SQL Database capabilities for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d59f5-104">SYNTAX</span></span>

### <span data-ttu-id="d59f5-105">FilterResults (padrão)</span><span class="sxs-lookup"><span data-stu-id="d59f5-105">FilterResults (Default)</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d59f5-106">Defaultresults</span><span class="sxs-lookup"><span data-stu-id="d59f5-106">DefaultResults</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d59f5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d59f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d59f5-108">O cmdlet **Get-AzureRmSqlCapability** Obtém os recursos de banco de dados SQL do Azure disponíveis na assinatura atual para uma região.</span><span class="sxs-lookup"><span data-stu-id="d59f5-108">The **Get-AzureRmSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="d59f5-109">Se você especificar os parâmetros *ServerVersionName* , *editionname* ou *userobjecname* , esse cmdlet retornará os valores especificados e seus predecessores.</span><span class="sxs-lookup"><span data-stu-id="d59f5-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="d59f5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d59f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d59f5-111">Exemplo 1: obter recursos para a assinatura atual para uma região</span><span class="sxs-lookup"><span data-stu-id="d59f5-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="d59f5-112">Esse comando retorna os recursos para instâncias de banco de dados SQL na assinatura atual da região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d59f5-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="d59f5-113">Exemplo 2: obter recursos padrão para a assinatura atual para uma região</span><span class="sxs-lookup"><span data-stu-id="d59f5-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="d59f5-114">Esse comando retorna os recursos padrão para bancos de dados SQL na assinatura atual na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d59f5-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="d59f5-115">Exemplo 3: obter detalhes de um objetivo de serviço</span><span class="sxs-lookup"><span data-stu-id="d59f5-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="d59f5-116">Esse comando obtém recursos padrão para bancos de dados SQL para o objetivo de serviço especificado na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d59f5-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="d59f5-117">OS</span><span class="sxs-lookup"><span data-stu-id="d59f5-117">PARAMETERS</span></span>

### <span data-ttu-id="d59f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59f5-118">-DefaultProfile</span></span>
<span data-ttu-id="d59f5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d59f5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d59f5-120">-Padrões</span><span class="sxs-lookup"><span data-stu-id="d59f5-120">-Defaults</span></span>
<span data-ttu-id="d59f5-121">Indica que esse cmdlet obtém apenas padrões.</span><span class="sxs-lookup"><span data-stu-id="d59f5-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-122">-Editionname</span><span class="sxs-lookup"><span data-stu-id="d59f5-122">-EditionName</span></span>
<span data-ttu-id="d59f5-123">Especifica o nome da edição de banco de dados para a qual este cmdlet obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="d59f5-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="d59f5-124">-LocationName</span></span>
<span data-ttu-id="d59f5-125">Especifica o nome do local para o qual este cmdlet obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="d59f5-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="d59f5-126">Para obter mais informações, consulte regiões do Azure https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="d59f5-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="d59f5-127">-ServerVersionName</span></span>
<span data-ttu-id="d59f5-128">Especifica o nome da versão do servidor para a qual este cmdlet obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="d59f5-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-129">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="d59f5-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="d59f5-130">Especifica o nome do objetivo do serviço para o qual este cmdlet obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="d59f5-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d59f5-131">-Confirm</span></span>
<span data-ttu-id="d59f5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d59f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d59f5-133">-WhatIf</span></span>
<span data-ttu-id="d59f5-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d59f5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d59f5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d59f5-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59f5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59f5-136">CommonParameters</span></span>
<span data-ttu-id="d59f5-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59f5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59f5-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59f5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59f5-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d59f5-139">INPUTS</span></span>

### <span data-ttu-id="d59f5-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d59f5-140">None</span></span>
<span data-ttu-id="d59f5-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d59f5-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d59f5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d59f5-142">OUTPUTS</span></span>

### <span data-ttu-id="d59f5-143">Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="d59f5-143">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="d59f5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d59f5-144">NOTES</span></span>

## <span data-ttu-id="d59f5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d59f5-145">RELATED LINKS</span></span>
