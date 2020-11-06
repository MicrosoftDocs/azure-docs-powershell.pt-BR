---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428777"
---
# <span data-ttu-id="766c6-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="766c6-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="766c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="766c6-102">SYNOPSIS</span></span>
<span data-ttu-id="766c6-103">Executa um bloco de script do Windows PowerShell em um nó.</span><span class="sxs-lookup"><span data-stu-id="766c6-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="766c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="766c6-104">SYNTAX</span></span>

### <span data-ttu-id="766c6-105">ByName</span><span class="sxs-lookup"><span data-stu-id="766c6-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="766c6-106">BySession</span><span class="sxs-lookup"><span data-stu-id="766c6-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="766c6-107">DESCRIPTION</span></span>
<span data-ttu-id="766c6-108">O cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** executa um bloco de script do Windows PowerShell em um nó gerenciado por um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="766c6-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="766c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="766c6-109">EXAMPLES</span></span>

## <span data-ttu-id="766c6-110">OS</span><span class="sxs-lookup"><span data-stu-id="766c6-110">PARAMETERS</span></span>

### <span data-ttu-id="766c6-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="766c6-111">-Command</span></span>
<span data-ttu-id="766c6-112">Especifica o bloco de script a ser executado no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="766c6-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766c6-113">-DefaultProfile</span></span>
<span data-ttu-id="766c6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="766c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766c6-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="766c6-115">-NodeName</span></span>
<span data-ttu-id="766c6-116">Especifica o nome do nó no qual executar o bloco de script.</span><span class="sxs-lookup"><span data-stu-id="766c6-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="766c6-117">-PowerShellSessionName</span></span>
<span data-ttu-id="766c6-118">Especifica o nome do espaço de execução do Windows PowerShell no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="766c6-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="766c6-119">-RawOutput</span></span>
<span data-ttu-id="766c6-120">Indica que o cmdlet retorna o objeto completo que contém a saída do nó.</span><span class="sxs-lookup"><span data-stu-id="766c6-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="766c6-122">Especifica o nome do grupo de recursos ao qual o nó pertence.</span><span class="sxs-lookup"><span data-stu-id="766c6-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-123">-Sessão</span><span class="sxs-lookup"><span data-stu-id="766c6-123">-Session</span></span>
<span data-ttu-id="766c6-124">Especifica o objeto de **sessão** que este cmdlet usa para se conectar ao nó de destino.</span><span class="sxs-lookup"><span data-stu-id="766c6-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="766c6-125">Esse parâmetro pode ser especificado em vez dos parâmetros *ResourceGroupName* , *NodeName* , *SessionName* e *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="766c6-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-126">-SESSIONNAME</span><span class="sxs-lookup"><span data-stu-id="766c6-126">-SessionName</span></span>
<span data-ttu-id="766c6-127">Especifica o nome da sessão para gerenciar o nó.</span><span class="sxs-lookup"><span data-stu-id="766c6-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766c6-128">CommonParameters</span></span>
<span data-ttu-id="766c6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766c6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="766c6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766c6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="766c6-131">INPUTS</span></span>

### <span data-ttu-id="766c6-132">Sessão</span><span class="sxs-lookup"><span data-stu-id="766c6-132">Session</span></span>
<span data-ttu-id="766c6-133">O parâmetro ' Session ' aceita o valor do tipo ' Session ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="766c6-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="766c6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="766c6-134">OUTPUTS</span></span>

### <span data-ttu-id="766c6-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="766c6-135">System.Object</span></span>

## <span data-ttu-id="766c6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="766c6-136">NOTES</span></span>

## <span data-ttu-id="766c6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="766c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="766c6-138">Cmdlets de gerenciamento do Azure Server</span><span class="sxs-lookup"><span data-stu-id="766c6-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


