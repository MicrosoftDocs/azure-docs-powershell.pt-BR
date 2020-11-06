---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d6e9ac96a5263add451fb03eae7783fe344852fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427150"
---
# <span data-ttu-id="ac984-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ac984-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="ac984-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac984-102">SYNOPSIS</span></span>
<span data-ttu-id="ac984-103">Obtém a política de detecção de ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="ac984-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac984-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac984-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac984-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac984-105">DESCRIPTION</span></span>
<span data-ttu-id="ac984-106">O cmdlet **Get-AzureRmSqlServerThreatDetectionPolicy** Obtém a política de detecção de ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac984-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="ac984-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor para o qual esse cmdlet obtém a política.</span><span class="sxs-lookup"><span data-stu-id="ac984-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="ac984-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac984-108">EXAMPLES</span></span>

### <span data-ttu-id="ac984-109">Exemplo 1: obter a política de detecção de ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="ac984-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="ac984-110">Este comando obtém a política de detecção de ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="ac984-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="ac984-111">O servidor é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac984-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ac984-112">OS</span><span class="sxs-lookup"><span data-stu-id="ac984-112">PARAMETERS</span></span>

### <span data-ttu-id="ac984-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac984-113">-DefaultProfile</span></span>
<span data-ttu-id="ac984-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ac984-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac984-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac984-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac984-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="ac984-116">Specifies the name of the resource group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac984-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ac984-117">-ServerName</span></span>
<span data-ttu-id="ac984-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ac984-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac984-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac984-119">-Confirm</span></span>
<span data-ttu-id="ac984-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac984-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac984-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac984-121">-WhatIf</span></span>
<span data-ttu-id="ac984-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac984-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac984-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac984-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac984-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac984-124">CommonParameters</span></span>
<span data-ttu-id="ac984-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac984-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac984-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac984-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac984-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac984-127">INPUTS</span></span>

### <span data-ttu-id="ac984-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac984-128">System.String</span></span>

## <span data-ttu-id="ac984-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac984-129">OUTPUTS</span></span>

### <span data-ttu-id="ac984-130">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ac984-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="ac984-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac984-131">NOTES</span></span>

## <span data-ttu-id="ac984-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac984-132">RELATED LINKS</span></span>

[<span data-ttu-id="ac984-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ac984-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="ac984-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ac984-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


