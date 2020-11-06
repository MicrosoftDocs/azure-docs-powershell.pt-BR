---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430643"
---
# <span data-ttu-id="b90dd-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="b90dd-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="b90dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b90dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b90dd-103">Executa um bloco de script do Windows PowerShell em um nó.</span><span class="sxs-lookup"><span data-stu-id="b90dd-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b90dd-104">SYNTAX</span></span>

### <span data-ttu-id="b90dd-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b90dd-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90dd-106">BySession</span><span class="sxs-lookup"><span data-stu-id="b90dd-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b90dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b90dd-107">DESCRIPTION</span></span>
<span data-ttu-id="b90dd-108">O cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** executa um bloco de script do Windows PowerShell em um nó gerenciado por um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="b90dd-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="b90dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b90dd-109">EXAMPLES</span></span>

## <span data-ttu-id="b90dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="b90dd-110">PARAMETERS</span></span>

### <span data-ttu-id="b90dd-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="b90dd-111">-Command</span></span>
<span data-ttu-id="b90dd-112">Especifica o bloco de script a ser executado no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="b90dd-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b90dd-113">-NodeName</span></span>
<span data-ttu-id="b90dd-114">Especifica o nome do nó no qual executar o bloco de script.</span><span class="sxs-lookup"><span data-stu-id="b90dd-114">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="b90dd-115">-PowerShellSessionName</span></span>
<span data-ttu-id="b90dd-116">Especifica o nome do espaço de execução do Windows PowerShell no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="b90dd-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="b90dd-117">-RawOutput</span></span>
<span data-ttu-id="b90dd-118">Indica que o cmdlet retorna o objeto completo que contém a saída do nó.</span><span class="sxs-lookup"><span data-stu-id="b90dd-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="b90dd-120">Especifica o nome do grupo de recursos ao qual o nó pertence.</span><span class="sxs-lookup"><span data-stu-id="b90dd-120">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-121">-Sessão</span><span class="sxs-lookup"><span data-stu-id="b90dd-121">-Session</span></span>
<span data-ttu-id="b90dd-122">Especifica o objeto de **sessão** que este cmdlet usa para se conectar ao nó de destino.</span><span class="sxs-lookup"><span data-stu-id="b90dd-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="b90dd-123">Esse parâmetro pode ser especificado em vez dos parâmetros *ResourceGroupName* , *NodeName* , *SessionName* e *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="b90dd-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-124">-SESSIONNAME</span><span class="sxs-lookup"><span data-stu-id="b90dd-124">-SessionName</span></span>
<span data-ttu-id="b90dd-125">Especifica o nome da sessão para gerenciar o nó.</span><span class="sxs-lookup"><span data-stu-id="b90dd-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90dd-126">-DefaultProfile</span></span>
<span data-ttu-id="b90dd-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b90dd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b90dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90dd-128">CommonParameters</span></span>
<span data-ttu-id="b90dd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90dd-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90dd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b90dd-131">INPUTS</span></span>

### <span data-ttu-id="b90dd-132">Sessão</span><span class="sxs-lookup"><span data-stu-id="b90dd-132">Session</span></span>
<span data-ttu-id="b90dd-133">O parâmetro ' Session ' aceita o valor do tipo ' Session ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b90dd-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="b90dd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b90dd-134">OUTPUTS</span></span>

### <span data-ttu-id="b90dd-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="b90dd-135">System.Object</span></span>

## <span data-ttu-id="b90dd-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b90dd-136">NOTES</span></span>

## <span data-ttu-id="b90dd-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b90dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="b90dd-138">Cmdlets de gerenciamento do Azure Server</span><span class="sxs-lookup"><span data-stu-id="b90dd-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


