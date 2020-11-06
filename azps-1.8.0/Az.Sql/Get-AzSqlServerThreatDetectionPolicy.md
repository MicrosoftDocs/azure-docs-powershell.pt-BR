---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598932"
---
# <span data-ttu-id="d8b56-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8b56-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="d8b56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8b56-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b56-103">Obtém a política de detecção de ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="d8b56-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="d8b56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8b56-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8b56-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b56-106">O cmdlet **Get-AzSqlServerThreatDetectionPolicy** Obtém a política de detecção de ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b56-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="d8b56-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor para o qual esse cmdlet obtém a política.</span><span class="sxs-lookup"><span data-stu-id="d8b56-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="d8b56-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8b56-108">EXAMPLES</span></span>

### <span data-ttu-id="d8b56-109">Exemplo 1: obter a política de detecção de ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="d8b56-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="d8b56-110">Este comando obtém a política de detecção de ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="d8b56-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="d8b56-111">O servidor é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8b56-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d8b56-112">OS</span><span class="sxs-lookup"><span data-stu-id="d8b56-112">PARAMETERS</span></span>

### <span data-ttu-id="d8b56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b56-113">-DefaultProfile</span></span>
<span data-ttu-id="d8b56-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d8b56-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b56-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8b56-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="d8b56-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="d8b56-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d8b56-117">-ServerName</span></span>
<span data-ttu-id="d8b56-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8b56-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d8b56-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8b56-119">-Confirm</span></span>
<span data-ttu-id="d8b56-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8b56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b56-121">-WhatIf</span></span>
<span data-ttu-id="d8b56-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8b56-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b56-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8b56-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b56-124">CommonParameters</span></span>
<span data-ttu-id="d8b56-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b56-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8b56-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b56-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8b56-127">INPUTS</span></span>

### <span data-ttu-id="d8b56-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b56-128">System.String</span></span>

## <span data-ttu-id="d8b56-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8b56-129">OUTPUTS</span></span>

### <span data-ttu-id="d8b56-130">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d8b56-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="d8b56-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8b56-131">NOTES</span></span>

## <span data-ttu-id="d8b56-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8b56-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8b56-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8b56-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="d8b56-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8b56-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


